<template>
  <div>
    <h1>作用域插槽</h1>
    <hr />
    <Todo :todos="todos">
      <!--
       v-slot:通过一个对象接受子组件回传的数据
      -->
      <template #="{row,$inde}">
           <pre :style="{color:row.done?'green':'red'}">{{row.title}}</pre>
      </template>
    </Todo>
  </div>
</template>

<script setup lang="ts">
import Todo from "./Todo.vue";
//响应式数据
import { ref } from "vue";

let todos = ref([
  { id: 1, title: "吃饭", done: false },
  { id: 2, title: "睡觉", done: true },
  { id: 3, title: "打豆豆", done: true },
]);
</script>

<style scoped>
</style>