<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/products">Products</router-link>
      <router-link to="/cart">Cart</router-link>
      <router-link to="/checkout">Checkout</router-link>
    </nav>

    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  background-color: #f0f0f0; /* Light gray background */
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
}

nav {
  background-color: #007bff; /* Blue navigation bar */
  padding: 10px;
  display: flex;
  justify-content: space-around;
  width: 100%;
}

nav a {
  color: #fff; /* White text */
  text-decoration: none;
  font-weight: bold;
  padding: 5px 10px;
  transition: background-color 0.3s;
}

nav a:hover {
  background-color: #0056b3; /* Darker blue on hover */
}

router-link-exact-active {
  background-color: #0056b3; /* Darker blue for active link */
}
</style>

