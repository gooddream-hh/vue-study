<template>
 <div class="category">
     <h3>{{title}}分类</h3>
    <slot name="1" :games="games1"></slot>
    <slot name="2" :games="games2"></slot>
 </div>
</template>

<script>
export default {
  name:'Category',
  props:['title'],
    data(){
    return{
      games1:['4399','斗地主','王者荣耀','和平精英'],
      games2:['我的世界','cf','LOL','cs']
    }
  }
}
</script>

<style>
  .category{
      background-color:aqua;
      width: 200px;
      height: 300px;
  }
  h3{
      background-color: orange;
      text-align: center;
  }
</style>