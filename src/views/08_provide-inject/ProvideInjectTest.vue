<template>
  <div>
    <h1>我是爷爷{{token}}</h1>
    <hr />
    <Child></Child>
  </div>
</template>

<script setup lang="ts">
import Child from "./Child.vue";

//提供数据
import { provide, ref } from "vue";
let token = ref(new Date());
//两个参数:第一个参数K 第二个参数V
provide("TOKEN",token);
</script>

<style scoped>
</style>