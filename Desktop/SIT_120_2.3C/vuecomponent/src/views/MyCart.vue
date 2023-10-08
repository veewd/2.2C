<template>
  <div>
    <h1>Cart</h1>
    <ul>
      <li v-for="item in cart" :key="item.id">{{ item.name }} - ${{ item.price }}</li>
    </ul>
    <!-- Updated router link to pass 'cart' data as a query parameter -->
    <router-link :to="{ path: '/checkout', query: { cart: cart } }">Proceed to Checkout</router-link>
  </div>
</template>

<script>
import { inject } from 'vue';

export default {
  setup() {
    const cart = inject('cart');

    return {
      cart,
    };
  },
};
</script>
