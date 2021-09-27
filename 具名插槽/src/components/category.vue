<template>
 <div class="category">
     <h3>{{title}}分类</h3>
     <!-- 定义一个插槽，等着组件的使用者进行填充 -->
    <slot name="center">这里可以填写默认值，当组件使用者没有进行填充时，会显示</slot>
    <slot name="foot">这里可以填写默认值，当组件使用者没有进行填充时，会显示</slot>
 </div>
</template>

<script>
export default {
  name:'Category',
  props:['listData','title']
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