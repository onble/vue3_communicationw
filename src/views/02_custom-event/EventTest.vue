<template>
  <div>
    <h1>vue3事件相关</h1>
    <pre @click="handler(1,2,$event)">
       大奖东去浪淘尽,千古风流人物
    </pre>
    <div @haha="handler1">我是一个div</div>
    <hr>
    <Event1 @getCar="handler2"></Event1>
    <hr>
    <!--下面这种就是原生DOM事件--->
    <!--相当于给组件根节点绑定DOM事件+事件委派-->
    <Event2 @click="handler3" @xxx="handler4"></Event2>
  </div>
</template>

<script setup lang="ts">
//事件:原生DOM事件、组件通信方式自定义事件
//事件回调
//引入子组件
import Event1 from './Event1.vue';
import Event2 from './Event2.vue';
const handler = (a,b,event)=>{
   console.log('原生DOM事件',event);
}
//div自定义事件的回调--没有任何意义
const handler1 = ()=>{

}
//第一个子组件绑定自定义事件回调
const handler2 = (car)=>{
  console.log('接收到儿子给的'+car)
}

//第二个子组件绑定事件
const handler3 = (event)=>{
   console.log(event);
}

const handler4 = (a,b,c)=>{
   console.log(a,b,c);
}
</script>

<style scoped>
</style>