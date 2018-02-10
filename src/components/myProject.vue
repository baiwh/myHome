<template>
  <div class="project">
    <div v-for="(item,index) in info" class="projectDiv">
      <div>
        <img v-bind:src="'./../../static/'+item.srcImg+'.png'" alt=""
        v-bind:style="">
      </div>
      <div class="projectInfo">
        <h2>{{item.name}}</h2>
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
            pInfo1: [
              '这是一个前后端分离的任务管理网站',
            ],
            pInfo2: [
              '啦啦'
            ],
            pInfo3: [
              '啦啦'
            ]
          },
          {
            ind: '项目经验2',
            srcImg: 'lift',
            name: 'jQuery版lift',
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
              '实现了进度条动态随CheckBox动态变化的效果',
              '实现了编辑时input切换的效果',
              '自定义实现了年月日选择列表的动画效果',
              '实现了时间轴的显示效果',
              '通过大量的Ajax实现了页面无刷新保存和修改数据'
            ]
          },
          {
            ind: '项目经验3',
            srcImg: 'myWeb1',
            name: '个人页面',
            pInfo1: [
              '这是两个H5和JavaScript的练手网页',
              '自定义实现了鼠标悬浮放大，移动显示等效果',
              '实现了页面在小窗口和横竖屏的自适应',
            ],
            pInfo2: [],
            pInfo3: []
          },
          {
            ind: '项目经验4',
            srcImg: 'myWeb3',
            name: '个人页面',
            pInfo1: [
              '这是两个H5和JavaScript的练手网页',
              '自定义实现了悬浮导航栏，轮播图等效果',
              '实现了鼠标悬浮移出，图片散拢的效果'
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
  .projectUl{
    margin: 2vh 2vw;
  }

</style>
