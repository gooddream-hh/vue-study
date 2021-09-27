<template>
 <div class="container">    
    <Category title="游戏">  
       <template v-slot:default="obj">
        <ul>
          <li v-for="(g,index) in obj.games" :key="index">{{g}}</li>
        </ul>  
       </template>
    </Category>
    <Category title="游戏">  
      <!-- 默认插槽的简便写法 -->
       <template v-slot="obj">
        <ol>
        <li v-for="(g,index) in obj.games" :key="index">{{g}}</li>
      </ol>
       </template>
    </Category>
  
    <Category title="游戏"> 
      <!-- 解构插槽 -->
       <template v-slot="{games}">
        <h4 v-for="(g,index) in games" :key="index">{{g}}</h4>
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
