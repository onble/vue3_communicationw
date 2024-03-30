<template>
    <div class="box">
        <h1>作用域插槽</h1>
        <p>{{ todos }}</p>
        <!-- <ul>
            <li
                :style="{ color: item.done ? 'green' : 'red' }"
                v-for="(item, index) in todos"
                :key="item.id"
            >
                {{ item.title }}
            </li>
        </ul> -->
        <ul>
            <li v-for="(item, index) in todos" :key="item.id">
                <!-- 作用域插槽：可以将数据回传给父组件 -->
                <slot :$row="item" :$index="index"></slot>
            </li>
        </ul>
    </div>
</template>

<script setup lang="ts">
// 通过props接收父组件传递数据
defineProps(["todos"]);
</script>

<style scoped>
.box {
    width: 100vw;
    height: 400px;
    background: skyblue;
}
</style>