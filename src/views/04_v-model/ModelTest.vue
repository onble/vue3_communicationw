<template>
  <div>
    <h1>vue3测试v-model:实现父子组件数据同步</h1>
    <input type="text" placeholder="请你输入密码" v-model="msg" />
    <h2>v-model实现父子组件数据同步{{ money }}</h2>
    <!-- 
      v-model实现父子组件数据同步:
       <Child :value="money" @input="handler"></Child>
     -->
    <!-- vue3:
         给子组件传递                props modelValue 
         给子组件绑定的自定义事件名字 update:modelValue
     -->
    <Child v-model="money"></Child>
    <hr />
    <h1>一个子组件使用多个v-model语法{{cnGDP}}{{bzGDP}}</h1>
    <Child1 v-model:pageNo="cnGDP" v-model:pageSize="bzGDP"></Child1>
  </div>
</template>

<script setup lang="ts">
//v-model:收集表单数据->数据双向绑定
import Child1 from "./Child1.vue";
import { ref } from "vue";
import Child from "./Child.vue";
//收集表单数据
let msg = ref("");
//父亲的钱
let money = ref(1000);
let cnGDP = ref(10000);
let bzGDP = ref(100);
//Child子组件自定义事件的回调
const handler = (num) => {
  money.value = num;
};
</script>

<style scoped>
</style>