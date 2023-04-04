<template>
  <div>
    <h1>学习$attrs与$listeners</h1>
    <hr>
    <!-- my-button:咱们自己封装的按钮,在使用属性与属性值写法与element-plus里面按钮写法一样 -->
    <my-button type="success" size="small" title="成功按钮" @click="handler" @xxx="handler"></my-button>
  </div>
</template>

<script setup lang="ts">
//引入自己封装按钮
import MyButton from './MyButton.vue'

const handler = ()=>{

}
</script>

<style scoped>
</style>