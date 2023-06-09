<script setup>
import {ref} from "vue";

const name = ref('Vue.js')

function greet(event) {
  alert(`Hello ${name.value}!`)
  // `event` 是 DOM 原生事件
  if (event) {
    alert(`tag name : ` + event.target.tagName)
  }
}
</script>

<template>
  <h2>方法事件处理器</h2>
  <!-- `greet` 是上面定义过的方法名 -->
  <button @click="greet">Greet</button>
</template>

<style scoped>

</style>
