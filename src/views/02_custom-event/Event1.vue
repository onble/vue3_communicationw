<template>
  <div class="box">
    <h1>我是子组件event1</h1>
    <!--下面这种写法:vue2写法-->
    <button @click="$emit('getCar', '法拉利')">给父组件送一台车</button>
    <button @click="sendCar">给父组件送一火车汽车</button>
  </div>
</template>

<script setup lang="ts">
//使用一个方法defineEmits方法去获取$emit方法,触发自定义事件
//defineEmits不需要引入直接使用
let $emit: any = defineEmits(['getCar']);
//组合式API书写地方
const sendCar = () => {
  $emit("getCar", "三本子");
};
</script>


<style scoped>
.box {
  width: 400px;
  height: 200px;
  background: red;
}
</style>