<template>
  <div>
    <h1>我是父组件:props学习</h1>
    <hr />
    <Child money="666" :car="car"></Child>
  </div>
</template>

<script setup lang="ts">
import Child from "./Child.vue";
import { ref } from "vue";
//定义车
let car = ref("法拉利");
</script>

<style scoped>
</style>