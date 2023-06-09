<script setup>
function say(message) {
  alert(message)
}
</script>

<template>
  <h2>在内联处理器中调用方法</h2>
  <button @click="say('hello')">Say hello</button>
  <button @click="say('bye')">Say bye</button>
</template>

<style scoped>

</style>
