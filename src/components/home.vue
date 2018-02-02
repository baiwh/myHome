<template>
  <div>
    <personal></personal>
    <my-project></my-project>
  </div>
</template>

<script>
  import personal from './personal.vue'
  import myProject from './myProject.vue'
  export default {
    name: 'home',
    data() {
      return {}
    },
    components:{
      personal:personal,
      myProject:myProject
    },

  }
</script>
<style>

</style>
