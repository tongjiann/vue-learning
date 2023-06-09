<script setup>
import {ref} from "vue";

const welcome = ref("welcomeClass")
</script>

<template>
  <label :class="welcome">Welcome to my project about learning vue</label>
</template>

<style scoped>

.welcomeClass {
  margin-top: 100px;
  font-size: 50px;
}

</style>
