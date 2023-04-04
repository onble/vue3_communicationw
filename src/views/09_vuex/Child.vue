<template>
  <div>
    <h1>我是子组件{{ money }}</h1>
    <button @click="sendMoney(1000000)">点击父子组件数据同步</button>
  </div>
</template>

<script setup lang="ts">
defineProps(["money"]);
let emit5 = defineEmits(["update:money"]);
const sendMoney = (num) => {
   emit5('update:money',num)
};
</script>

<style scoped>
</style>