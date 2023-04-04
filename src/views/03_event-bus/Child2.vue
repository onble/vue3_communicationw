<template>
  <div class="cz">
    <h1>我是曹植</h1>
    <button @click="handler">点击我给你送一板砖</button>
  </div>
</template>

<script setup lang="ts">
import bus from '../../utils/bus';
//按钮回调
const handler = ()=>{
  //事件类型
  bus.emit('sendData','搬砖');
}
</script>

<style scoped>
.cz {
  width: 100%;
  height: 100px;
  background: pink;
}
</style>