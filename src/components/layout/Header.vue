<template>
  <div id="header">
    <ul>
      <li> <router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped>
ul{
    margin:0;
    padding: 0;
  }
  li{
    display: inline;
    margin-right: 10px;
  }
</style>