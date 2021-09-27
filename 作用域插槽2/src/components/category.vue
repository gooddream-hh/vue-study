<template>
 <div class="category">
     <h3>{{title}}分类</h3>
    <slot :games="games">默认插槽</slot>
 </div>
</template>

<script>
export default {
  name:'Category',
  props:['title'],
    data(){
    return{
    
      games:['4399','斗地主','王者荣耀','和平精英']
     
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