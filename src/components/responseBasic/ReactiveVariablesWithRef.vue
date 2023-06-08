<script setup>
import {ref} from "vue";

const count = ref(0)

console.log(count) // { value: 0 }
console.log(count.value) // 0

count.value++
console.log(count.value) // 1
</script>

<template>
  <h2>用 ref() 定义响应式变量</h2>
</template>

<style scoped>

</style>
