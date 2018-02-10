<template>
    <div>
      <ul class="infoUl">
        <li v-for="item in myProjectInfo"><a href="">{{item}}</a></li>
      </ul>
    </div>
</template>

<script>
  export default {
    name: 'projectInfo',
    data() {
      return {}
    },
    props: [
      'pInfo'
    ],
    computed: {
      myProjectInfo(){
        return this.pInfo;
      }
    }
  }
</script>
<style>
  .infoUl{
    margin: 15px;
  }
</style>
