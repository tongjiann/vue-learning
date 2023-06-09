<script setup>
function doThis() {
  console.log("do this ")
}
</script>

<template>
  <h2>事件修饰符</h2>
  <!-- 单击事件将停止传递 -->
  <a @click.prevent="doThis" href="https://www.baidu.com">...</a>

  <!-- 提交事件将不再重新加载页面 -->
  <form @submit.prevent="onSubmit"></form>

  <!-- 修饰语可以使用链式书写 -->
  <a @click.stop.prevent="doThat"></a>

  <!-- 也可以只有修饰符 -->
  <form @submit.prevent></form>

  <!-- 仅当 event.target 是元素本身时才会触发事件处理器 -->
  <!-- 例如：事件处理器不来自子元素 -->
  <div @click.self="doThat">...</div>
</template>

<style scoped>

</style>
