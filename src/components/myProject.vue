<template>
  <div class="project">
    <div v-for="(item,index) in info" class="projectDiv">
      <div>
        <img v-bind:src="'./../../static/'+item.srcImg+'.png'" alt=""
        v-bind:style="">
      </div>
      <div class="projectInfo">
        <a v-bind:href="item.link"><h2>{{item.name}}<img src="./../assets/link.png" alt=""></h2></a>
        <ul class="projectUl">
          <li><h3>项目简介</h3></li>
          <project-info v-bind:pInfo="item.pInfo1"></project-info>
          <li v-if="item.pInfo2!=''"><h3>开发中 填过的坑 和 总结的笔记</h3></li>
          <note-list v-bind:pInfo="item.pInfo2" v-if="item.pInfo2!=''"></note-list>
          <li v-if="item.pInfo3!=''"><h3>实现的一些效果</h3></li>
          <project-info v-bind:pInfo="item.pInfo3" v-if="item.pInfo3!=''"></project-info>
        </ul>
      </div>
      <hr class="projectHr" v-if="index<3">
    </div>
  </div>
</template>
<script>
  import projectInfo from './projectInfo.vue'
  import noteList from './noteList.vue'
  export default {
    name: 'myProject',
    data() {
      return {
        info: [
          {
            ind: '项目经验1',
            srcImg: 'sign',
            name: 'Vue版lift',
            link:'http://www.codinghou.com/vueLift/',
            pInfo1: [
              '这是一个独立完成的前后端分离的任务管理网站',
              '是用vue和vuex重构的lift',
              '左侧导航部分使用了vue-router',
              '数据的交互使用了axios'
            ],
            pInfo2: [
              'axios跨域请求的处理',
              '在父组件中调用子组件中的方法',
              'vuex和axios的结合使用',
              'v-model对于checked初始化以及自定义可输入元素的影响'
            ],
            pInfo3: [
              '通过vuex处理子组件向父组件传递信息',
              '使用v-for的情况下checkBox的单选和多选',
              '使用v-for的情况下控制各个元素的显示和隐藏、class和style的切换、初始化样式的不同',
              '筛选数据的多选和单选'
            ]
          },
          {
            ind: '项目经验2',
            srcImg: 'lift',
            name: 'jQuery版lift',
            link:'http://www.codinghou.com/index/index.action',
            pInfo1: [
              '这是和后台一起开发的任务管理网站',
              '主要负责网站的页面设计，JavaScript、css、HTML的编写',
              '配合后端进行了JavaScript和页面的修改、联调和测试',
              '与后台的数据交互大部分使用Ajax，少数页面使用表单提交'
            ],
            pInfo2: [
              '事件冒泡的处理',
              'js动态生成DOM，绑定事件失效的问题',
              'Ajax异步和其他function执行顺序的问题',
              '输入框根据内容大小自适应的问题'
            ],
            pInfo3: [
              '自定义实现了登录页面密码强弱判断的动画效果',
              '自定义实现了CheckBox打钩的动画效果',
              '自定义实现了年月日选择列表的动画效果',
              '通过大量的Ajax实现了页面无刷新保存和修改数据'
            ]
          },
          {
            ind: '项目经验3',
            srcImg: 'myWeb1',
            link:'',
            name: '个人页面',
            pInfo1: [
              '这是一个H5、js、jQuery的练手网页',
              '页面采用了弹性布局',
              '自定义实现了鼠标悬浮放大，移动显示等效果',
              '实现了页面在小窗口和横竖屏的自适应',
            ],
            pInfo2: [],
            pInfo3: []
          },
          {
            ind: '项目经验4',
            srcImg: 'myWeb3',
            link:'',
            name: '个人页面',
            pInfo1: [
              '这是一个H5、js、jQuery的练手网页',
              '自定义实现了悬浮导航栏，轮播图等效果',
              '实现了鼠标悬浮时的移出、散拢、显示和隐藏、放大等效果'
            ],
            pInfo2: [],
            pInfo3: []
          }
        ]
      }
    },
    components: {
      projectInfo: projectInfo,
      noteList:noteList
    }
  }
</script>
<style>
  .project {
    width: 70vw;
    margin: 3% 15%;
    padding: 4vw;
    float: left;
    z-index: 5;
  }
  .projectDiv {
    width: 62vw;
    float: left;
  }
  .projectHr{
    background: #dcdcdc;
    height: 1px;
    width: 62vw;
    margin: 5vh 0;
    float: left;
    border-radius: 70%;
    border: transparent;
  }
  .project img {
    max-width: 20vw;
    float: left;
    margin: 2vw;
    max-height: 20vw;
  }

  .projectInfo {
    width: 35vw;
    float: right;
  }
  .projectInfo img{
    height: 25px;
    width: 25px;
    float: left;
    margin: 0;
    left: 23vw;
    top: 1vh;
  }
  .projectUl{
    margin: 2vh 2vw;
  }

</style>
