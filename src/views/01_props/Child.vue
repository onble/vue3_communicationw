<template>
  <div>
    <h1>我是子组件Child</h1>
    <h2>使用父组件传递过来的数据{{ car }}</h2>
    <button @click="updateCar">修改父亲传递过来的props数据</button>
  </div>
</template>

<script setup lang="ts">
//defineProps方法,不需要引入直接使用
//作用是接受父组件传递过来的props数据
//defineProps函数执行:返回一个代理对象,通过代理对象的属性接受父组件传递过来数据
let props = defineProps(["money", "car"]);
//注意:模板使用props(代理对象:可以直接书写代理对象属性的名字直接使用)
//但是在script标签内部不能省略props.xxxx
const updateCar = ()=>{
   //props.car = 'xxx'.
   //props数据只能读不能修改！！！
}



</script>

<style scoped>
</style>