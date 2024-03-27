<template>
    <div class="child">
        <p>我是子组件2</p>
        <button @click="handler">点击我触发自定义事件xxx</button>
        <button @click="$emit('click', 'AK47', 'J20')">
            点击我触发自定义事件click
        </button>
    </div>
</template>

<script setup lang="ts">
// 利用defineEmits方法返回函数触发自定义事件
// defineEmits方法不需要引入直接使用
// let $emit = defineEmits(["xxx"]);
let $emit = defineEmits(["xxx", "click"]);
// console.log($emit);
// (event, ...args) => instance.emit(event, ...args)
//按钮点击回调
const handler = () => {
    // console.log(this);
    // undifined
    // 第一个参数：事件类型 第二个|第三个|第N个参数即为注入数据
    $emit("xxx", "东风导弹", "航母");
};
</script>

<style scoped>
.child {
    width: 400px;
    height: 200px;
    background: pink;
}
</style>