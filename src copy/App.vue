<template>
 <div class="container">
  <!--  <Category title="美食" :listData="foods">
   </Category>
   <Category title="游戏" :listData="games"/>
   <Category title="电影" :listData="films"/> -->

    <Category title="美食" :listData="foods">
     <img src="https://img2.baidu.com/it/u=4117582627,679171248&fm=253&fmt=auto&app=120&f=JPEG?w=500&h=500" alt="">
   </Category>
    <Category title="游戏" >
      <ul>
        <li v-for="(g,index) in games" :key="index">{{g}}</li>
      </ul>
    </Category>
   <Category title="电影">
     <video controls src="http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4"></video>
   </Category>
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
      foods:['火锅','烧烤','小龙虾','海里捞'],
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
