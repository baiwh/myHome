<template>
  <div id="trueBody">
    <home-nav></home-nav>
    <div class="bg">
      <!--<img v-bind:src="'./../../static/'+backgroundSrc" alt="">-->
    </div>
    <personal></personal>
    <div class="projectBg">
      <my-project></my-project>
    </div>
    <div class="window">
      <my-note></my-note>
    </div>
    <div id="other">
      <div class="skill">
        <ul>
          <li v-for="item in skillInfo">{{item}}</li>
        </ul>
      </div>
      <div class="github">
        <img src="./../../static/github.png" alt="">
      </div>
      <div class="otherImg">
        <img src="./../assets/me.png" alt="">
        <img src="./../assets/github.png" alt="">
      </div>
    </div>
    <footer class="footer" id="try">
      <div class="center">
        <img src="./../assets/beian.png"/>
        <a target="_blank"
           href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=13010402001501">
          冀公网安备 13010402001501号
        </a>
        <a target="_blank" href="http://www.miitbeian.gov.cn">冀ICP备17021530号-2</a>
      </div>
    </footer>
  </div>
</template>

<script>
  import personal from './personal.vue'
  import myProject from './myProject.vue'
  import myNote from './myNote.vue'
  import homeNav from './homeNav.vue'
  export default {
    name: 'home',
    data() {
      return {
        skillInfo: [
          '开发语言：HTML、css 和 JavaScript 。熟悉 Jquery、vue、vuex、axios',
          '版本管理工具：熟悉 git 管理工具，了解从搭建本地版本库，连接远程仓库，以及基本的版本控制操作',
          '开发工具：熟悉 webStorm，Hbuilder',
          '熟悉 chrome 前端调试工具',
          '熟悉 MarkDown 语法，日常写文档使用 。熟悉 Photoshop 的一般操作，切图修图等'
        ]
      }
    },
    components: {
      personal: personal,
      myProject: myProject,
      myNote: myNote,
      homeNav: homeNav
    }
  }
</script>
<style>
  #trueBody {
    float: left;
  }

  .bg {
    z-index: 1;
    background: url("./../../static/bg.jpg") no-repeat;
    background-size: 100% 100%;
    position: fixed;
    height: 100vh;
    width: 100vw;
  }

  .bg img {
    height: 100%;
    width: 100%;
  }

  .projectBg {
    width: 100vw;
    background: #ffffff;
    float: left;
  }

  .window {
    height: 100vh;
    width: 100vw;
    background: rgba(0, 0, 0, 0.3);
    /*background: transparent;*/
    float: left;
  }
  #other{
    height: 100vh;
    width: 100vw;
    float: left;
    /*background: #ffffff;*/
  }
  .skill{
    height: 50vh;
    float: left;
  }
  .skill li{

  }
  .github img{
    height: 50vh;
  }
  .otherImg{

  }
  .otherImg img{

  }

  footer {
    width: 100vw;
    color: #dcdcdc;
    float: left;
    border-top: 1px solid #dcdcdc;
    background: #ffffff;
  }

  .footer a {
    margin: 10px;
    line-height: 1.5;
    color: #979797;
  }

  .center {
    transform: translate(-50%, 0);
    float: left;
    left: 50%;
    margin: 10px;
  }
</style>
