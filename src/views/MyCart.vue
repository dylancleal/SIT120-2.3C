<template>
  <div class="cart-page">
    <h1 class="page-title">Cart</h1>
    <ul class="cart-items">
      <li v-for="item in cart" :key="item.id" class="cart-item">
        {{ item.name }} - ${{ item.price }}
      </li>
    </ul>
    <router-link to="/checkout" class="proceed-to-checkout-button">Proceed to Checkout</router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cart: []  // Fetch this from a central store or API call in a real-world scenario.
    }
  }
}
</script>

<style scoped>
.cart-page {
  background-color: #f0f0f0; /* Light gray background */
  padding: 20px;
  text-align: center;
}

.page-title {
  font-size: 28px;
  color: #007BFF; /* Blue title color */
}

.cart-items {
  list-style-type: none;
  padding: 0;
}

.cart-item {
  font-size: 16px;
  margin: 10px 0;
  padding: 5px;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.proceed-to-checkout-button {
  background-color: #007BFF; /* Blue background */
  color: #fff; /* White text color */
  text-decoration: none;
  display: inline-block;
  padding: 10px 20px;
  margin-top: 20px;
  border-radius: 5px;
  font-size: 16px;
}

.proceed-to-checkout-button:hover {
  background-color: #0056b3; /* Darker blue on hover */
}
</style>
