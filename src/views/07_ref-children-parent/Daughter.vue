<template>
    <div class="dau">
        <h1>我是闺女曹杰:{{ money }}</h1>
        <button @click="handler($parent)">点击我爸爸给我10000元</button>
        <!-- 传入的名字就是$parent -->
    </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
// 闺女钱数
let money = ref(999999);
// 闺女按钮点击回调
const handler = ($parent) => {
    money.value += 10000;
    console.log($parent);
    // Proxy(Object)
    // 需要父亲将数据进行对外暴露
    $parent.money -= 10000;
};
</script>

<style scoped>
.dau {
    width: 300px;
    height: 300px;
    background: hotpink;
}
</style>