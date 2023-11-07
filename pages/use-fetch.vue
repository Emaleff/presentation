<template>
  <div>
    <h1>
      nuxt предоставляет для работы с апи useAsyncData и useFetch useFetch
      является оберткой для useAsyncData так же nuxt предоставляет useLazyFetch
      и useLazyAsyncData, которые не блокируют навигацию в период загрузки
    </h1>

    <h2>
      хуки useHead и useSeoMeta предоставляют возможность менять head стариницы
    </h2>
    <div>
      хук useState предоставляет возможность обмена данными через между
      компонентами с поддержкой ssr
      <br />
      Поскольку данные внутри useState будут сериализованы в JSON, важно, чтобы
      они не содержали ничего, что не может быть сериализовано, например
      классов, функций или символов.
    </div>

    <h2>хук useNuxtData предоставляет доступ к кешированым данным</h2>
    <h2>хук useCookie предоставляет доступ к куки {{ cookie }}</h2>
    <h2>client-only отображает свой слот только на стороне клиента</h2>
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

// useSeoMeta({
//   title: "My Amazing Site",
//   ogTitle: "My Amazing Site",
//   description: "This is my amazing site, let me tell you all about it.",
//   ogDescription: "This is my amazing site, let me tell you all about it.",
//   ogImage: "https://favicomatic.com/img/favic-o-matic.png",
//   twitterCard: "summary_large_image",
// });
</script>

<style scoped lang="scss"></style>
