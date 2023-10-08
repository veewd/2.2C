<template>
  <div class="my-products-container">
    <!-- Page title using text interpolation -->
    <h1>{{ pageTitle }}</h1>

    <!-- List of products using v-for with an object -->
    <div class="product" v-for="product in products" :key="product.id">
      <!-- Product name using text interpolation -->
      <h2>{{ product.name }}</h2>
      <!-- Product price using text interpolation -->
      <p>Price: ${{ product.price }}</p>
      <!-- Add to cart button with a click event listener -->
      <button @click="addToCart(product)">Add to Cart</button>
    </div>
    
    <!-- Router link to navigate to the cart component -->
    <router-link to="/cart">View Cart</router-link>
    
    <!-- Display cart data provided by App.vue -->
    <div class="cart-info">
      <h2>Cart Info:</h2>
      <ul>
        <li v-for="item in cart" :key="item.id">{{ item.name }} - ${{ item.price }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
import { ref, inject } from 'vue'; // Import the 'inject' function

export default {
  name: 'ProductList', // Renamed the component to "ProductList"
  setup() {
    // Page title using ref() for reactivity
    const pageTitle = ref('Products');
    
    // List of products
    const products = ref([
      { id: 1, name: 'PS5', price: 699 }, // Updated price without '$'
      { id: 2, name: 'Macbook Air', price: 1299 }, // Updated price without '$'
    ]);

    // Use the 'inject' function to access the 'cart' data provided by 'App.vue'
    const cart = inject('cart');

    // Add to cart method
    const addToCart = (product) => {
      // Add product to the cart
      cart.value.push(product);
    };

    // Return data and methods for setup
    return {
      pageTitle,
      products,
      addToCart,
      cart, // Make cart accessible in the template
    };
  },
};
</script>

<style scoped>
/* Styling using CSS classes and inline styles */
.products-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.product {
  border: 1px solid #ddd;
  padding: 20px;
  margin: 10px;
  text-align: center;
  background-color: #f9f9f9; /* Background color using inline styles */
}

button {
  background-color: #007bff;
  color: #fff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
}

.cart-info {
  margin-top: 20px;
}
</style>
