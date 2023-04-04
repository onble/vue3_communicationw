<template>
  <div :title="title">
      <!--人家element-plus组件提供 -->
     <el-button v-bind="$attrs">{{title}}</el-button>
  </div>
</template>

<script setup lang="ts">
//vue3组合式API方法:获取父亲传递数据方法useAttrs
import {useAttrs} from 'vue';
//获取父组件传递过来数据:三个属性[type,size,title]
//$attrs:可以获取到父亲传递过来的属性与方法(原生DOM|自定义事件)
let $attrs = useAttrs();
let props = defineProps(['title']);
</script>
<style scoped>
</style>