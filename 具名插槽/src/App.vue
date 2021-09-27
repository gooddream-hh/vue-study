<template>
 <div class="container">
  <!--  <Category title="美食" :listData="foods">
   </Category>
   <Category title="游戏" :listData="games"/>
   <Category title="电影" :listData="films"/> -->

    <Category title="照片" :listData="foods">
     <template v-slot:center>
        <img src="https://img2.baidu.com/it/u=4117582627,679171248&fm=253&fmt=auto&app=120&f=JPEG?w=500&h=500" alt="">
     </template>
     <template v-slot:foot>
      <a  href="https://image.baidu.com/search/index?tn=baiduimage&ct=201326592&lm=-1&cl=2&ie=gb18030&word=%B6%AF%C2%FE%CD%BC%C6%AC&fr=ala&ala=1&alatpl=normal&pos=0">更多照片</a>
     </template>  
   </Category>
    <Category title="游戏" >
      <template v-slot:center>
      <ul>
        <li v-for="(g,index) in games" :key="index">{{g}}</li>
      </ul>
      </template>
       <template v-slot:foot>
      <div  class="footer">
        <a href="https://www.csdn.net/">游戏1</a>
        <a href="https://www.csdn.net/">游戏2</a>
      </div>
      </template>
    </Category>
   <Category title="电影">
      <template v-slot:center>
     <video  controls src="http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4"></video>
     </template>
      <template v-slot:foot>
        <div class="footer">
        <a href="https://www.csdn.net/">经典</a>
        <a href="https://www.csdn.net/">热门</a>
        <a href="https://www.csdn.net/">推荐</a>
      </div>
      </template>
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
      //foods:['火锅','烧烤','小龙虾','海里捞'],
      games:['4399','斗地主','王者荣耀','和平精英'],
      //films:['《你好，李焕英》','《夏洛特烦扰》','《你的名字》','《蜘蛛侠》']
    }
  }
}
</script>

<style>
  .container, .footer{
    display: flex;
    justify-content:space-around;
  }
  /* 也可以写在组件中 */
  img,video{
    width: 200px;
    height: 200px;
  }
</style>
