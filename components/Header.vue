<template>
  <header class='header'>
    <ul class='nav-items'>
      <li><NuxtLink to="/" :class="{ active: isActive('index') }">Homepage</NuxtLink></li>
      <li><NuxtLink to="/users" :class="{ active: isActive('users') }">Users list</NuxtLink></li>
      <li><NuxtLink to="/products" :class="{ active: isActive('products') }">Products list</NuxtLink></li>
    </ul>
  </header>
</template>

<script>
export default {
  methods: {
    isActive(path) {
      return this.$route.name.match(path)
    }
  }
}
</script>

<style scoped>
  .header {
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #ccc;
  }

  .nav-items {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 80%;
  }

  .nav-items a {
    text-decoration: none;
    color: black;
  }

  .nav-items a.active {
    color: white;
    font-weight: bold;
  }
</style>