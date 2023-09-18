<template>
  <div class="checkout-page">
    <h1 class="page-title">Checkout</h1>
    <p class="total-amount">Total Amount: ${{ totalAmount }}</p>
    <button class="place-order-button" @click="placeOrder">Place Order</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cart: [], // Ideally, fetch this from a central store or API call.
    }
  },
  computed: {
    totalAmount() {
      return this.cart.reduce((sum, item) => sum + item.price, 0);
    }
  },
  methods: {
    placeOrder() {
      alert('Order placed successfully!');
      this.cart = []; // Clear the cart after placing the order. 
                      // In reality, you would send this to a backend service.
    }
  }
}
</script>

<style scoped>
.checkout-page {
  background-color: #f0f0f0; /* Light gray background */
  padding: 20px;
  text-align: center;
}

.page-title {
  font-size: 28px;
  color: #007BFF; /* Blue title color */
}

.total-amount {
  font-size: 18px;
  margin: 20px 0;
}

.place-order-button {
  background-color: #007BFF; /* Blue background */
  color: #fff; /* White text color */
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 5px;
  font-size: 16px;
}

.place-order-button:hover {
  background-color: #0056b3; /* Darker blue on hover */
}
</style>
