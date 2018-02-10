<template>
  <div class="note">
    <div class="notes" v-for="(item,index) in noteInfo">
      <h3>{{item.name}}</h3>
      <p>{{item.content}}</p>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'myNote',
    data() {
      return {
        noteInfo: [
          {
            name: '原生axios跨域（云端url）',
            content:'原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）' +
            '原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域' +
            '（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）' +
            '原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）'
          },
          {
            name: '原生axios跨域（云端url）',
            content:'原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）' +
            '原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域' +
            '（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）' +
            '原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）'
          },
          {
            name: '原生axios跨域（云端url）',
            content:'原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）' +
            '原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域' +
            '（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）' +
            '原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）原生axios跨域（云端url）'
          }
        ]
      }
    }
  }
</script>
<style>
  .note{
    width: 70vw;
    margin: 3% 15%;
    float: left;
    padding: 2vw;
  }
  .notes {
    width: 20vw;
    float: left;
    background: rgba(255,255,255,0.5);
    margin: 1vw;
    padding: 2vw;
  }
  .notes h3{
    margin-bottom: 1.5vw;
  }
  .notes p{
    line-height: 1.5;
  }
</style>
