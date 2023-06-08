<script setup>
import TemplateSyntaxComp from "@/components/templateSyntax/TemplateSyntaxComp.vue";
import {ref} from "vue";
import ReactivityFundamentalComp from "@/components/responseBasic/ReactivityFundamentalComp.vue";

const activeCompName = ref("ResponseBasic")


function updateActiveCompName(compName) {
  activeCompName.value = compName
}


</script>

<template>
  <div>
    <div>
      <button @click="updateActiveCompName('TemplateSyntaxComp')">TemplateSyntaxComp</button>
      <button @click="updateActiveCompName('ReactivityFundamentalComp')">ReactivityFundamentalComp</button>
    </div>
    <div/>
    <div v-if="activeCompName==='TemplateSyntaxComp'">
      <TemplateSyntaxComp/>
    </div>
    <div v-else-if="activeCompName==='ReactivityFundamentalComp'">
      <ReactivityFundamentalComp/>
    </div>
  </div>
</template>
<style>

</style>
