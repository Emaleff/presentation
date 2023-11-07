<template>
  <div><input type="text" v-model="TextValue" /> {{ TextValue }}</div>
</template>

<script setup lang="ts">
const TextValue = ref("");
</script>

<style scoped></style>
