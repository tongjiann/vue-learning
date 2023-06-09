<script setup>

import InlineHandler from "@/components/eventHanding/InlineHandler.vue";
import MethodHandler from "@/components/eventHanding/MethodHandler.vue";
import CallingMethodsInInlineHandler from "@/components/eventHanding/CallingMethodsInInlineHandler.vue";
import AccessingEventArgumenInInlineHandler from "@/components/eventHanding/AccessingEventArgumenInInlineHandler.vue";
import EventModifier from "@/components/eventHanding/EventModifier.vue";
</script>

<template>
  <h1>事件处理</h1>
  <InlineHandler/>
  <MethodHandler/>
  <CallingMethodsInInlineHandler/>
  <AccessingEventArgumenInInlineHandler/>
  <EventModifier/>
</template>

<style scoped>

</style>
