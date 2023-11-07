<template>
  <div>
    <h1>
      nuxt предоставляет для работы с апи useAsyncData и useFetch useFetch
      является оберткой для useAsyncData так же nuxt предоставляет useLazyFetch
      и useLazyAsyncData, которые не блокируют навигацию в период загрузки
    </h1>

    <h2>{{ cookie }}</h2>
  </div>
</template>

<script setup lang="ts">
const cookie = useCookie("uuid");

useHead({
  title: "какой то тайтл",
  link: [
    {
      rel: "icon",
      type: "image/x-icon",
      href: "https://s.yimg.com/rz/l/favicon.ico",
    },
  ],
});

useSeoMeta({
  title: "My Amazing Site",
  ogTitle: "My Amazing Site",
  description: "This is my amazing site, let me tell you all about it.",
  ogDescription: "This is my amazing site, let me tell you all about it.",
  ogImage: "https://favicomatic.com/img/favic-o-matic.png",
  twitterCard: "summary_large_image",
});
</script>

<style scoped lang="scss"></style>
