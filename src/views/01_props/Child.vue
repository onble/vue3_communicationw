<template>
    <div class="son">
        <h1>我是子组件：曹植</h1>
        <p>{{ props.info }}</p>
        <p>{{ props.money }}</p>
        <!-- props可以省略前面的名字 -->
        <p>{{ info }}</p>
        <p>{{ money }}</p>
        <button @click="updateProps">修改props数据</button>
    </div>
</template>
<!-- 
<script>
// vue2的选择式api，vue3也支持
export default {
    props: ["info", "money"],
};
</script>
-->

<script setup lang="ts">
// 使用组合式api，要写setup

// 需要使用到defineProps方法去接收父组件传递过来的数据
// defineProps是Vue3提供方法，不需要引入直接使用
let props = defineProps(["info", "money"]);
// 数组或对象写法，与vue2一样
// console.log(props);
// 返回的是Proxy代理对象
// 值不可以修改

// 按钮点击的回调
const updateProps = () => {
    // props.money += 10;
    // Cannot assign to 'money' because it is a read-only property.Vetur(2540)
    // Child.vue:33 [Vue warn] Set operation on key "money" failed: target is readonly. Proxy(Object) {info: '我是曹操', money: 10000}
    // console.log(info);
    // Cannot find name 'info'.Vetur(2304)
    //Uncaught ReferenceError: info is not defined
    // console.log(props.info);
    // 在script标签内props不可以省略，在templete里面可以
};
</script>

<style scoped>
.son {
    width: 400px;
    height: 200px;
    background: hotpink;
}
</style>