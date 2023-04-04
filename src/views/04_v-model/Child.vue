<template>
  <button>
    <span @click="$emit('update:modelValue',modelValue+1)">我是按钮组件{{modelValue}}</span>
  </button>
</template>

<script setup lang="ts">
//接受父组件传递过来props
let props = defineProps(['modelValue']);

//触发自定义事件
let $emit = defineEmits(['update:modelValue']);
</script>

<style scoped>
</style>