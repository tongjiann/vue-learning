<script setup>
import {reactive, watch} from "vue";

const obj = reactive({count: 0})

watch(()=>obj.count, (newValue, oldValue) => {
  // 在嵌套的属性变更时触发
  // 注意：`newValue` 此处和 `oldValue` 是相等的
  // 因为它们是同一个对象！
  console.log("touched" + "~".repeat(obj.count))
})

</script>

<template>
  <h2>深层侦听器</h2>
  <p>不是很懂</p>
  <input v-model="obj.count"/>
  <label>touched {{ obj.count }} times</label>
</template>

<style scoped>

</style>
