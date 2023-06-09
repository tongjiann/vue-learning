<script setup>

import {ref} from "vue";

const message = ref()
const text = ref()
const checked = ref(false)
const picked = ref()
const selected = ref()
const checkedNames = ref([])

const options = ref([
  {text: 'One', value: 'A'},
  {text: 'Two', value: 'B'},
  {text: 'Three', value: 'C'}
])

</script>

<template>
  <h2>基本用法</h2>
  <p>Message is: {{ message }}</p>
  <input v-model="message" placeholder="edit me"/>

  <span>Multiline message is:</span>
  <p style="white-space: pre-line;">{{ message }}</p>
  <textarea v-model="message" placeholder="add multiple lines"></textarea>
  <div/>
  <textarea v-model="text"></textarea>
  <div/>
  <input type="checkbox" id="checkbox" v-model="checked"/>
  <label for="checkbox">{{ checked }}</label>
  <div>Checked names: {{ checkedNames }}</div>

  <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
  <label for="jack">Jack</label>

  <input type="checkbox" id="john" value="John" v-model="checkedNames">
  <label for="john">John</label>

  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
  <label for="mike">Mike</label>

  <div>Picked: {{ picked }}</div>

  <input type="radio" id="one" value="One" v-model="picked"/>
  <label for="one">One</label>

  <input type="radio" id="two" value="Two" v-model="picked"/>
  <label for="two">Two</label>

  <div>Selected: {{ selected }}</div>

  <select v-model="selected">
    <option disabled value="">Please select one</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>

  <div>Selected: {{ selected }}</div>

  <select v-model="selected" multiple>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <div></div>
  <select v-model="selected">
    <option v-for="option in options" :value="option.value">
      {{ option.text }}
    </option>
  </select>

  <div>Selected: {{ selected }}</div>
</template>

<style scoped>

</style>
