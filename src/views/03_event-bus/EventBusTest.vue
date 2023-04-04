<template>
  <div class="box">
    <h1>我是曹操</h1>
    <hr />
    <Child1></Child1>
    <Child2></Child2>
  </div>
</template>

<script setup lang="ts">
import Child1 from "./Child1.vue";
import Child2 from "./Child2.vue";
</script>

<style scoped>
.box {
  width: 800px;
  height: 400px;
  background: yellowgreen;
}
</style>