<script setup>
import TemplateSyntaxComp from "@/components/templateSyntax/TemplateSyntaxComp.vue";
import {ref} from "vue";
import ReactivityFundamentalComp from "@/components/responseBasic/ReactivityFundamentalComp.vue";
import EventHandingComp from "@/components/eventHanding/EventHandingComp.vue";
import FormComp from "@/components/forms/FormComp.vue";
import LifeCycleComp from "@/components/lifecycle/LifeCycleComp.vue";
import Welcome from "@/components/welcome/Welcome.vue";

const activeCompName = ref("Welcome")
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
      <button @click="updateActiveCompName('FormComp')">FormComp</button>
      <button @click="updateActiveCompName('LifeCycleComp')">LifeCycleComp</button>
    </div>
    <div/>
    <div v-if="activeCompName==='Welcome'">
      <Welcome/>
    </div>
    <div v-else-if="activeCompName==='TemplateSyntaxComp'">
      <TemplateSyntaxComp/>
    </div>
    <div v-else-if="activeCompName==='ReactivityFundamentalComp'">
      <ReactivityFundamentalComp/>
    </div>
    <div v-else-if="activeCompName==='EventHandingComp'">
      <EventHandingComp/>
    </div>
    <div v-else-if="activeCompName==='FormComp'">
      <FormComp/>
    </div>
    <div v-else-if="activeCompName==='LifeCycleComp'">
      <LifeCycleComp/>
    </div>
  </div>
</template>
<style>
.title {
  font-size: 40px;
  margin-bottom: 30px;
}
</style>
