<template>
  <div>
    <h1>Checkout</h1>
    <p>Total Amount: \${{ totalAmount }}</p>
    <button @click="placeOrder">Place Order</button>
  </div>
</template>

<script>
export default {
  props: {
    cart: {
      type: Array,
      default: () => [], // Default value is an empty array
    },
  },
  computed: {
    totalAmount() {
      // Compute the total amount based on the cart prop
      return this.cart.reduce((sum, item) => sum + item.price, 0);
    },
  },
  methods: {
    placeOrder() {
      alert('Order placed successfully!');
      // In reality, you might want to send the order to a backend service.
      // You can clear the cart prop like this:
      // this.$emit('update:cart', []);
    },
  },
};
</script>
