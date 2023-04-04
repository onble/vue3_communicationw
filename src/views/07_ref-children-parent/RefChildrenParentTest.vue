<template>
  <div class="box">
    <h1>我是父组件:我有两个孩子存款{{money}}</h1>
    <button @click="borrowFromSon">点击我找儿子借500</button>
    <hr>
    <Son ref="son"></Son>
    <hr>
    <Dau></Dau>
  </div>
</template>

<script setup lang="ts">
import Son from './Son.vue'
import Dau from './Daughter.vue'
import { ref } from "vue";
//父组件的数据
let money = ref(10000);
//获取子组件实例:方法 + 数据
let son = ref();

//父亲的方法:按钮点击回调
const borrowFromSon = ()=>{
    //父亲的钱+500
    money.value +=500;
    son.value.money-=500;
}

defineExpose({money});
</script>

<style scoped>
</style>