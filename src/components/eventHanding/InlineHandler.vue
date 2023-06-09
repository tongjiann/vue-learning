<script setup>
import {ref} from "vue";

const cnt = ref(0)
</script>

<template>
  <h2>内联事件处理器</h2>
  <button @click="cnt++">Add 1</button>
  <p>Count is: {{ cnt }}</p>
</template>

<style scoped>

</style>
