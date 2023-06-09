<script setup>
import TemplateSyntaxComp from "@/components/templateSyntax/TemplateSyntaxComp.vue";
import {ref} from "vue";
import ReactivityFundamentalComp from "@/components/responseBasic/ReactivityFundamentalComp.vue";
import EventHandingComp from "@/components/eventHanding/EventHandingComp.vue";

const activeCompName = ref("ResponseBasic")
const titleClass = ref("title")

function updateActiveCompName(compName) {
  activeCompName.value = compName
}


</script>

<template>
  <div>
    <div :class="titleClass">Vue-Learning</div>
    <div>
      <button @click="updateActiveCompName('TemplateSyntaxComp')">TemplateSyntaxComp</button>
      <button @click="updateActiveCompName('ReactivityFundamentalComp')">ReactivityFundamentalComp</button>
      <button @click="updateActiveCompName('EventHandingComp')">EventHandingComp</button>
    </div>
    <div/>
    <div v-if="activeCompName==='TemplateSyntaxComp'">
      <TemplateSyntaxComp/>
    </div>
    <div v-else-if="activeCompName==='ReactivityFundamentalComp'">
      <ReactivityFundamentalComp/>
    </div>
    <div v-else-if="activeCompName==='EventHandingComp'">
      <EventHandingComp/>
    </div>
  </div>
</template>
<style>
.title {
  font-size: 40px;
  margin-bottom: 30px;
}
</style>
