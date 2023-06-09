<script setup>
import {ref} from "vue";

const pick = ref("first")
const first = ref("first")
const second = ref("second")
const toggle = ref()
const selected = ref()

</script>

<template>
  <h2>值绑定</h2>
  <label>{{ toggle }}</label>
  <input
      type="checkbox"
      v-model="toggle"
      true-value="yes"
      false-value="no"/>

  <div></div>
  <label>{{ pick }}</label>

  <input type="radio" v-model="pick" :value='first'/>
  <input type="radio" v-model="pick" :value='second'/>
  <div></div>
  <label>{{ selected }}</label>
  <select v-model="selected">
    <!-- 内联对象字面量 -->
    <option :value="{ number: 123 }">123</option>
  </select>

</template>

<style scoped>

</style>
