<template>
  <div class="container">
    <nav>
      <NuxtLink to="./"> main </NuxtLink>
      <NuxtLink to="./v-once"> v-once && v-memo </NuxtLink>
      <NuxtLink to="./nuxt-image"> NuxtImage </NuxtLink>
      <NuxtLink to="./keep-alive"> KeepAlive </NuxtLink>
      <NuxtLink to="./tanstack-query"> tanstack-query </NuxtLink>
      <NuxtLink to="./use-fetch"> хуки в NUXT </NuxtLink>
    </nav>

    <div>
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
const counter = useState("counter");
</script>
<style lang="scss">
.container {
  max-width: 1000px;
  margin: 0 auto;
}

nav {
  display: flex;
  gap: 20px;
}
</style>
