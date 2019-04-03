<template>
  <header>
    <h1>{{title}}</h1>
    <p>{{subtitle}}</p>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    title: String,
    subtitle: String,
  },
};
</script>

<style scoped>
  header {
    border: 10px solid #ffffff;
    padding: 20px;
    margin: 20px;
    text-align: left;
  }
</style>
