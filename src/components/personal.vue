<template>
  <div class="person">
    <img id="headImg" src="./../assets/head.jpg" alt="头像">
    <div class="psInfo">
      <h1>白文灏</h1>
      <h5><img src="./../assets/people.png" alt="">女 | 23岁 | 本科 | 应届毕业生</h5>
      <h5><img src="./../assets/email.png" alt="">hao1994430@vip.qq.com</h5>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'personal',
    methods: {
      copy: function () {
        document.execCommand('Copy')
      }
    }
  }
</script>
<style>
  .person {
    height: 100vh;
    width: 100vw;
    background: url("./../assets/0.png") no-repeat;
    background-size: 100% 100%;
  }

  #headImg {
    height: 10vmax;
    width: 10vmax;
    border-radius: 50%;
    transform: translate(-50%, -50%);
    top: 30vh;
    left: 50vw;
    position: absolute;
    /*cursor: pointer;*/
    z-index: 100;
  }

  .psInfo {
    text-align: center;
    top: 60vh;
  }

  .psInfo h1, .psInfo h5 {
    padding: 10px;
    width: 100vw;
    color: #ffffff;
    font-weight: 600;
  }

  .psInfo img {
    height: 15px;
    width: 15px;
    margin: 0px 10px;
    top: 2px;
  }
</style>
