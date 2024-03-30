<template>
    <div class="child1">
        <h1>孙子组件</h1>
        <p>{{ car }}</p>
        <button @click="updateCar">更新数据</button>
    </div>
</template>

<script setup lang="ts">
import { inject } from "vue";
// 注入祖先组件提供数据
// 需要参数：即为祖先提供数据的key
let car = inject("TOKEN");
// console.log(car);
// RefImpl {__v_isShallow: false, dep: undefined, __v_isRef: true, _rawValue: '法拉利', _value: '法拉利'}

const updateCar = () => {
    car.value = "自行车";
};
</script>

<style scoped>
.child1 {
    width: 200px;
    height: 200px;
    background: red;
}
</style>