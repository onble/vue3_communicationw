<template>
    <div class="child1">
        <h1>{{ infoStore.count }}</h1>
        <p @click="updateTodo">{{ todoStore.todos }}</p>
        <p>{{ todoStore.arr }}</p>
        <p>{{ todoStore.total }}</p>
    </div>
</template>

<script setup lang="ts">
import useInfoStore from "../../store/modules/info";
// 获取小仓库对象
let infoStore = useInfoStore();

// 引入组合式API函数仓库
import useTodoStore from "../../store/modules/todo";
let todoStore = useTodoStore();

// 点击p段落去修改仓库的数据
const updateTodo = () => {
    todoStore.updateTodo();
};
</script>

<style scoped>
.child1 {
    width: 200px;
    height: 200px;
    background: hotpink;
}
</style>