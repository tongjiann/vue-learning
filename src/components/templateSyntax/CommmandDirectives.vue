<script setup>
import {ref} from "vue";

const seen= ref(true)

function changeVisibility() {
  seen.value=  !seen.value
}
</script>

<template>
  <h2>指令 Directives</h2>
  <p v-if="seen" @click="changeVisibility()">Now you see me</p>
  <p v-else @click="changeVisibility()">Now I am Hide</p>
</template>

<style scoped>

</style>
