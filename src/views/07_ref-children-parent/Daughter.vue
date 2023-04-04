<template>
  <div class="dau">
    <h1>我是女儿存款:{{ money }}</h1>
    <button @click="sendMoney($parent)">给爸爸送1000+</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
let money = ref(2000000);
//闺女的方法
const sendMoney = ($parent)=>{
   money.value-=1000;
   $parent.money+=1000;
}

</script>

<style scoped>
.dau {
  width: 400px;
  height: 200px;
  background: hotpink;
}
</style>