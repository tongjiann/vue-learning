<script setup>
const rawHtml = "<span style=\"color: red\">This should be red.</span>"
</script>

<template>
  <h2>原始 HTML</h2>
  <p>Using text interpolation: {{ rawHtml }}</p>
  <p>Using v-html directive: <span v-html="rawHtml"></span></p>
</template>

<style scoped>

</style>
