<template>
  <div>
    <h1>组件通信手段v-model</h1>
    <h1>父组件的钱{{money}}</h1>
    <Child :money="money" @update:money="handler"></Child>
    <hr>
    <Child1 v-model="money"></Child1>
  </div>
</template>

<script setup lang="ts">
import Child from './Child.vue'
import Child1 from './Child1.vue';
import {ref} from 'vue';
let money = ref(3000);
const handler = (val)=>{
   money.value+=val;
}

const handler1 = (val)=>{
   money.value+=val;
}
</script>

<style scoped>
</style>