<script setup>

import {ref, watch, watchEffect} from "vue";

const source = ref("")
watch(source, (newValue, oldValue) => {
  // 立即执行，且当 `source` 改变时再次执行
  console.log("immediate")
}, {immediate: true})

const todoId = ref(1)
const data = ref(null)

// watch(todoId, async () => {
//   const response = await fetch(
//       `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
//   )
//   data.value = await response.json()
// }, {immediate: true})

watchEffect(async () => {
  const response = await fetch(
      `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
  )
  data.value = await response.json()
})
</script>

<template>
  <h2>即时回调的侦听器</h2>
  <h2>watchEffect()</h2>
  <input v-model="todoId">
  <p>{{ data }}</p>
</template>

<style scoped>

</style>
