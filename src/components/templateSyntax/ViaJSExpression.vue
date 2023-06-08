<script setup>

const date = "123"
function toTitleDate(date) {
  return "111"
}

function formatDate(date) {
  return "222"
}

</script>

<template>
  <h2>使用 JavaScript 表达式</h2>
  <time :title="toTitleDate(date)" :datetime="date">
    {{ formatDate(date) }}
  </time>
</template>

<style scoped>

</style>
