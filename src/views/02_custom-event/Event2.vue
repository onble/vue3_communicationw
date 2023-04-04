<template>
  <div class="box1">
    <h1>我是子组件Event2</h1>
    <p @click="send">我是一个段落</p>
  </div>
</template>

<script setup lang="ts">
let $emit = defineEmits(["xxx"]);
const send = () => {
  $emit("xxx",'火箭','飞机','大炮');
};
</script>

<style scoped>
.box1 {
  width: 400px;
  height: 200px;
  background: yellowgreen;
}
</style>