<script setup>
import {ref} from 'vue'

const titleClass = ref('title')
const isButtonDisabled = ref("True")

const objectOfAttrs = {
  id: 'container',
  class: 'wrapper'
}

function changeEnablity() {
  isButtonDisabled.value = !isButtonDisabled.value
}
</script>

<template>
  <h2>Attribute 绑定</h2>
  <div v-bind:id="titleClass"> hello</div>

  <button @click="changeEnablity">is button enabled :{{ !isButtonDisabled }}</button>
  <button :disabled="isButtonDisabled">Button</button>
  <div>
    <button v-bind="objectOfAttrs">Bind Button</button>
  </div>
</template>

<style scoped>
#title {
  color: blue;
}
.wrapper{
  color: #00ffff;
}
#container{
  font-size:40px
}
</style>
