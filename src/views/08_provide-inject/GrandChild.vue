<template>
  <div>
    <h1>我是孙子{{ token }}</h1>
    <button @click="token += '!'">修改爷爷提供数据</button>
  </div>
</template>

<script setup lang="ts">
import { inject } from "vue";
let token = inject("TOKEN");
console.log(token);
</script>

<style scoped>
</style>