<template>
 <div class="container">
   <Category title="动漫" :listData="cartoons">
   </Category>
   <Category title="游戏" :listData="games"/>
   <Category title="电影" :listData="films"/>
 </div>
</template>

<script>
import Category from './components/category.vue'

export default {
  name: 'App',
  components: {
    Category
  },
  data(){
    return{
      cartoons:['海贼王','名侦探柯南','一人之下','未闻花名'],
      games:['4399','斗地主','王者荣耀','和平精英'],
      films:['《你好，李焕英》','《夏洛特烦扰》','《你的名字》','《蜘蛛侠》']
    }
  }
}
</script>

<style>
  .container{
    display: flex;
    justify-content:space-around;
  }
  /* 也可以写在组件中 */
  img,video{
    width: 200px;
    height: 200px;
  }
</style>
