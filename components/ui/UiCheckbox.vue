<template>
  <div><input type="checkbox" v-model="checkboxValue" /> checkboxValue</div>
</template>

<script setup lang="ts">
const checkboxValue = ref(false);
</script>

<style scoped></style>
