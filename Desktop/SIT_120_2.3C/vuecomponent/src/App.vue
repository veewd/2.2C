<template>
  <div id="app">
    <nav class="navbar">
      <router-link to="/" class="nav-link">Home</router-link>
      <router-link to="/products" class="nav-link">Products</router-link>
      <router-link to="/cart" class="nav-link">Cart</router-link>
      <router-link to="/checkout" class="nav-link">Checkout</router-link>
    </nav>

    <!-- Use the provide/inject pattern to share data -->
    <router-view />
  </div>
</template>

<script>
import { provide, ref } from 'vue'; // Import 'ref' from Vue

export default {
  setup() {
    const cart = ref([]); // Define the cart data here

    provide('cart', cart); // Provide the cart data to child components

    return {
      // You can include other setup logic here if needed
    };
  },
};
</script>

<style>
/* Add CSS styling for the navigation bar */
.navbar {
  background-color: #333; /* Background color */
  color: #fff; /* Text color */
  padding: 10px 0; /* Padding at the top and bottom */
  text-align: center;
}

.nav-link {
  color: #fff; /* Text color for links */
  text-decoration: none; /* Remove underlines from links */
  margin: 0 10px; /* Margin between links */
  font-size: 18px; /* Font size for links */
}

/* Style for active link (you can add more styles based on your preference) */
.nav-link.active {
  font-weight: bold; /* Make the active link bold */
}
</style>
