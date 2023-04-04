<template>
  <div class="son">
    <h1>我是儿子存款:{{money}}</h1>
  </div>
</template>

<script setup lang="ts">
import {ref} from 'vue';
let money = ref(200);

//外部访问对外暴露
defineExpose({money})
</script>

<style scoped>
.son {
  width: 400px;
  height: 200px;
  background: #ccc;
}
</style>