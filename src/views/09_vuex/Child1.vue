<template>
  <div>
    <h1>我是子组件{{ modelValue }}</h1>
    <button @click="emit7('update:modelValue',100000)">点击父子组件数据同步</button>
  </div>
</template>

<script setup lang="ts">
defineProps(["modelValue"]);
let emit7 = defineEmits(["update:modelValue"]);
</script>

<style scoped>
</style>