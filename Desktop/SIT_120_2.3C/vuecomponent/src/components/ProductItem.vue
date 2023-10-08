<template>
  <div class="product-item">
    <img :src="product.image" alt="Product Image" />
    <h2>{{ product.name }}</h2>
    <p>{{ product.description }}</p>
    <p>\${{ product.price }}</p>
    <button @click="addToCartAndNavigate(product)">Add to Cart</button>
  </div>
</template>

<script>
export default {
  props: {
    product: Object
  },
  methods: {
    addToCartAndNavigate(product) {
      // Clone the current query object
      const newQuery = { ...this.$route.query };

      // Check if a 'cart' query parameter already exists
      if (!newQuery.cart) {
        // If not, create it as an array with the current product's ID
        newQuery.cart = [product.id];
      } else {
        // If it already exists, add the current product's ID to the array
        newQuery.cart.push(product.id);
      }

      // Use the router to navigate to the '/cart' route with the updated query
      this.$router.push({ path: '/cart', query: newQuery });
    }
  }
}
</script>

