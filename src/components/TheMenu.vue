<template>
  <nav>
    <div class="links">
      <img src="@/assets/console.png" />
      <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </div>
    </div>
    <div></div>
  </nav>
</template>

<script>
export default {
  name: 'TheMenu',
};
</script>

<style scoped>
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 20px;
  }
  img {
    width: 50px;
  }
  a {
    color: #ffffff;
    padding: 20px 10px;
    text-transform: uppercase;
    text-decoration: none;
  }
  .links {
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
