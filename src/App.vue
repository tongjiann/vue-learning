<script>
import {ref} from 'vue';

import TemplateSyntaxComp from "@/components/templateSyntax/TemplateSyntaxComp.vue";
import ReactivityFundamentalComp from "@/components/responseBasic/ReactivityFundamentalComp.vue";
import EventHandingComp from "@/components/eventHanding/EventHandingComp.vue";
import FormComp from "@/components/forms/FormComp.vue";
import LifeCycleComp from "@/components/lifecycle/LifeCycleComp.vue";
import Welcome from "@/components/welcome/Welcome.vue";
import WatcherComp from "@/components/watchers/WatcherComp.vue";
import TemplateRefComp from "@/components/template-refs/TemplateRefComp.vue";

export default {
  components: {
    Welcome,
    TemplateSyntaxComp,
    ReactivityFundamentalComp,
    EventHandingComp,
    FormComp,
    LifeCycleComp,
    WatcherComp,
    TemplateRefComp
  },
  setup() {
    const activeCompName = ref('Welcome');
    const titleClass = 'title';

    const components = [
      'TemplateSyntaxComp',
      'ReactivityFundamentalComp',
      'EventHandingComp',
      'FormComp',
      'LifeCycleComp',
      'WatcherComp',
      'TemplateRefComp',
    ];

    function updateActiveCompName(compName) {
      activeCompName.value = compName;
    }

    return {
      activeCompName,
      titleClass,
      components,
      updateActiveCompName,
    };
  },
};
</script>

<template>
  <div>
    <div :class="titleClass">Vue-Learning</div>
    <button
        v-for="comp in components"
        :key="comp"
        @click="updateActiveCompName(comp)"
        :class="{ active: activeCompName === comp }"
    >
      {{ comp }}
    </button>
    <component :is="activeCompName"/>
  </div>
</template>

<style>
.title {
  font-size: 40px;
  margin-bottom: 30px;
}

button.active {
  /* 添加选中按钮的样式 */
  font-weight: bold;
  background-color: cyan;
}
</style>
