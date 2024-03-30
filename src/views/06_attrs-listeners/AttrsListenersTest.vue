<template>
    <div>
        <h1>useAttrs</h1>
        <el-button type="primary" size="small" :icon="Edit"></el-button>
        <HintButton
            type="primary"
            size="small"
            :icon="Edit"
            title="编辑按钮"
            @click="handler"
            @xxx="handler"
        ></HintButton>
    </div>
</template>

<script setup lang="ts">
// vue3框架提供一个方法useAtters方法，它可以获取组件身上的属性与事件！！！
// 图标组件
import {
    Check,
    Delete,
    Edit,
    Message,
    Search,
    Star,
} from "@element-plus/icons-vue";
import HintButton from "./HintButton.vue";
const handler = () => {
    alert(12306);
};
</script>

<style scoped>
</style>