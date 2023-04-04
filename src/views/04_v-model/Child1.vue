<template>
  <div>
    <button @click="$emits('update:pageNo',pageNo+1)">中国GDP{{ pageNo }}</button>
    <button @click="$emits('update:pageSize',pageSize+1)">韩国GDP{{ pageSize }}</button>
  </div>
</template>

<script setup lang="ts">
//接受父组件传递过来props
defineProps(["pageNo", "pageSize"]);
let $emits = defineEmits(["update:pageNo", "update:pageSize"]);
</script>

<style scoped>
</style>