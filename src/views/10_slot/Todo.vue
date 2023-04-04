<template>
  <div>
    <ul>
      <li v-for="(item, index) in todos" :key="item.id">
        <!--vue框架提供的全局组件-->
        <!--
           :row="item",并非props给slot传递数据
           就是作用域插槽的语法,将儿子内部数据回传父组件
        --->
        <slot :row="item" :$index="index" a='111'></slot>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
//接受父组件传递过来的数据
defineProps(["todos"]);
</script>

<style scoped>
</style>