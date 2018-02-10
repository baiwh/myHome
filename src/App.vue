<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'App'
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    float: left;
  }

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    position: relative;
    z-index: 5;
  }

  a {
    text-decoration: none;
    color: cornflowerblue;
  }
  h1,h2{
    text-align: center;
  }
  li{
    line-height: 1.5;
  }
</style>
