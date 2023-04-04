<template>
  <div class="cp">
    <h1>我是曹丕</h1>
  </div>
</template>

<script setup lang="ts">
import { onMounted } from "vue";
import bus from "../../utils/bus";
onMounted(() => {
  bus.on("sendData", (params) => {
    console.log(params);
  });
});
</script>

<style scoped>
.cp {
  width: 100%;
  height: 100px;
  background: red;
}
</style>