<template>
    <div class="box">
        <h1>我是子组件默认插槽</h1>
        <!-- 默认插槽 -->
        <slot></slot>
        <h1>我是子组件默认插槽</h1>
        <h1>我是子组件a插槽</h1>
        <slot name="a"></slot>
        <h1>我是子组件a插槽</h1>
        <h1>我是子组件b插槽</h1>
        <slot name="b"></slot>
        <h1>我是子组件b插槽</h1>
    </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.box {
    width: 100vw;
    height: 400px;
    background: skyblue;
}
</style>