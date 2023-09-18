<template>
  <div class="product-page">
    <h1 class="page-title">Products</h1>
    <div class="product-list">
      <product-item 
        v-for="product in products" 
        :key="product.id" 
        :product="product" 
        @add-to-cart="addToCart"
      ></product-item>
    </div>
  </div>
</template>

<script>
import ProductItem from '../components/ProductItem.vue'

export default {
  components: {
    ProductItem
  },
  data() {
    return {
      products: [
        { id: 1, name: 'Product A', price: 50 },
        { id: 2, name: 'Product B', price: 150 },
        // ... other products
      ],
      cart: []
    }
  },
  methods: {
    addToCart(product) {
      this.cart.push(product);
    }
  }
}
</script>

<style>
.product-page {
  background-color: #f0f0f0; /* Light gray background */
  padding: 20px;
  text-align: center;
}

.page-title {
  font-size: 28px;
  color: #007BFF; /* Blue title color */
}

.product-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.product-item {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
  text-align: center;
  background-color: #fff;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
  border-radius: 5px;
}

.product-item h2 {
  font-size: 18px;
  margin-bottom: 5px;
}

.product-item button {
  background-color: #007BFF; /* Blue background */
  color: #fff; /* White text color */
  border: none;
  padding: 5px 10px;
  cursor: pointer;
  border-radius: 3px;
  font-size: 14px;
}

.product-item button:hover {
  background-color: #0056b3; /* Darker blue on hover */
}
</style>
