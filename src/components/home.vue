<template>
  <div id="trueBody">
    <div class="bg">
      <!--<img v-bind:src="'./../../static/'+backgroundSrc" alt="">-->
    </div>
    <personal></personal>
    <div class="window">
      <div>项目经验</div>
    </div>
    <div class="projectBg">
      <my-project></my-project>
    </div>
    <div class="noteBg">
      <my-note></my-note>
    </div>
    <footer class="footer">
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
  export default {
    name: 'home',
    data() {
      return {}
    },
    components: {
      personal: personal,
      myProject: myProject,
      myNote: myNote
    },
    computed: {
      backgroundSrc(){
//          let scroll=document.getElementById('trueBody').scrollTop;
//            if(scroll<3000){
//                return 'bg.jpg';
//            }else {
//                return 'lift.png';
//            }
      }
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

  .window {
    height: 80vh;
    width: 100vw;
    background: rgba(0, 0, 0, 0.3);
    /*background: transparent;*/
    float: left;
  }

  .window div {
    color: #ffffff;
    float: left;
    font-size: 50px;
    transform: translate(-50%, -50%);
    top: 50%;
    left: 50%;
  }

  .projectBg {
    width: 100vw;
    background: #ffffff;
    float: left;
  }

  .noteBg {
    background: url("./../../static/sky.jpg") no-repeat;
    background-size: 100% 100%;
    float: left;
    width: 100vw;
    height: 100vh;
  }

  footer {
    width: 100vw;
    background: #dcdcdc;
    float: left;
  }

  .footer a {
    margin: 10px;
    line-height: 1.5;
  }

  .center {
    transform: translate(-50%,0);
    float: left;
    left: 50%;
    margin: 10px;
  }
</style>
