<template>
  <div class="container">
    <h1>layout</h1>

    <nav>
      <NuxtLink to="./"> main </NuxtLink>
      <NuxtLink to="./v-once"> v-once && v-memo </NuxtLink>
    </nav>

    <div>
      <slot />
    </div>
  </div>
</template>

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
