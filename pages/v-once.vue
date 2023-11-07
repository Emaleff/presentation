<template>
  <div>
    <h1>v-once && v-memo</h1>
    <div>{{ count }} Not directive</div>
    <div v-once>{{ count }} v-once</div>
    <div v-memo="[count === 5]">{{ count }} v-memo</div>
  </div>
</template>

<script setup lang="ts">
const count = ref(0);

setInterval(() => {
  count.value += 5;
}, 5000);
</script>

<style scoped lang="scss"></style>
