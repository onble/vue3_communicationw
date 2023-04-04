<template>
  <div style="background: #ccc; height: 50px;">
    <span>小明每次花100元</span>
    <button @click="handler">花钱</button>
    爸爸还剩 {{money}} 元
  </div>
</template>
<script type="text/ecmascript-6">
export default {
   props:['money'],
   methods:{
     handler(){
       this.$emit('update:money',this.money-100)
     }
   }
}
</script>
