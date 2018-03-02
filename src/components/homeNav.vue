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
    mounted:function(){

      if(this.getScroll>500){
          this.showNav='1';
      }
    },
    computed:{
      getScroll:function() {
        var scrollTop = 0;
        if (document.documentElement && document.documentElement.scrollTop) {
          scrollTop = document.documentElement.scrollTop;
        } else if (document.body) {
          scrollTop = document.body.scrollTop;
        }
        return scrollTop;
      },
    },
    methods: {
      navShow(){
        let height = document.body.scrollTop;
      },
      getScrolla:function() {
        var scrollTop = 0;
        if (document.documentElement && document.documentElement.scrollTop) {
          scrollTop = document.documentElement.scrollTop;
        } else if (document.body) {
          scrollTop = document.body.scrollTop;
        }
        return scrollTop;
      },
      navClick:function(){
        function sroll() {
          var scrollTop = 0;
          if (document.documentElement && document.documentElement.scrollTop) {
            scrollTop = document.documentElement.scrollTop;
          } else if (document.body) {
            scrollTop = document.body.scrollTop;
          }
          return scrollTop;
        }
        alert(sroll());
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
