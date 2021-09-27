<template>
 <div class="container">    
    <Category title="游戏">  
       <template v-slot:[dynamicSlotName]="obj">
        <ol>
          <li v-for="(g,index) in obj.games" :key="index">{{g}}</li>
        </ol>
       </template>
    </Category>
    <button style="width:120px" @click="change">点这切换</button>
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
      dynamicSlotName:'1'
    }
  },
  methods:{
    change(){
        if(this.dynamicSlotName=='1'){
          this.dynamicSlotName='2';
        }else
          this.dynamicSlotName='1';
    }
  }
}
</script>

<style>
  .container{
    display: flex;
    flex-direction: column;
  }
  /* 也可以写在组件中 */
  img,video{
    width: 200px;
    height: 200px;
  }
</style>
