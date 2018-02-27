<template>
  <div class="nav">
    <div v-for="(item,index) in navInfo" class="navDiv">
      <img v-bind:src="'./../../static/'+item.imgSrc+'.png'" alt="" v-on:click="navClick(index)">
      <span v-if="index>0" v-show="showNav==index">{{item.name}}</span>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'homeNav',
    data() {
      return {
        navInfo: [
          {
            'imgSrc': 'home',
            'name': 'home'
          },
          {
            'imgSrc': 'project',
            'name': '个人项目'
          },
          {
            'imgSrc': 'note2',
            'name': '笔记'
          },
          {
            'imgSrc': 'other',
            'name': 'about me'
          }
        ],
        showNav: '0'
      }
    },
    mounted(){
      window.addEventListener('scroll',this.navShow);
    },
    methods: {
      navShow(){
        let height = document.body.scrollTop;
      },
      navClick(event){
//        let height = document.getElementById('app').;
        let a=document.body.offsetTop;
//        let b=a
        alert(a);
      }
    }
  }
</script>
<style>
  .nav {
    right: 10px;
    position: fixed;
    z-index: 100;
    transform: translate(0, -50%);
    top: 50vh;
  }

  .navDiv {
    margin: 3vh 0;
    float: right;
    clear: right;
  }

  .navDiv img {
    height: 30px;
    width: 30px;
    float: left;
    margin: 0 10px;
    cursor: pointer;
  }

  .navDiv span {
    line-height: 30px;
    display: block;
    float: left;
    text-align: center;
    width: 80px;
    color: #e89abe;
  }
</style>
