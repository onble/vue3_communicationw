<template>
    <div :title="title">
        <!-- <h1>123</h1> -->
        <!-- <h1>{{ type }}</h1> -->
        <!-- <el-button :type="$attrs.type"></el-button> -->
        <el-button :="$attrs"></el-button>
        <h1 v-bind="{ a: 1, b: 2 }">123</h1>
    </div>
</template>

<script setup lang="ts">
// 接受父组件传递过来数据
// defineProps(["type", "size", "icon"]);
import { useAttrs } from "vue";
// console.log(useAttrs);
// ƒ useAttrs() {
//   return getContext().attrs;
// }

// 此方法执行会返回一个对象
let $atters = useAttrs();
// console.log($atters);
// Proxy(Object) {type: 'primary', size: 'small', icon: {…}, __vInternal: 1}

// 万一用props接收title
let props = defineProps(["title"]);
// console.log(props);
// console.log($atters);
// 两个人只有一个能拿到

// props与useAtters方法都可以获取父组件传递过来的属性与属性值
// 但是props接受了useAtters方法就获取不到了

console.log($atters);
</script>

<style>
</style>