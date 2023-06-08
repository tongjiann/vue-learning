<script setup>
import {nextTick, reactive} from 'vue'

const state = reactive({count: 0})

function increment() {
  state.count++
  nextTick(() => {
    // 访问更新后的 DOM
  })
}
</script>

<template>
  <button @click="increment">
    {{ state.count }}

  </button>
</template>
