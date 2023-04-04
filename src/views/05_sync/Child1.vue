<template>
  <div class="box">
    <span @click="emit6('update:visite',6666666)">小明每次花100元{{visite}}</span>
  </div>
</template>
<script lang="ts" setup>
 defineProps(['visite']);
 let emit6 = defineEmits(['update:visite'])
</script>
