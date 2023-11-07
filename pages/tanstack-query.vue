<template>
  <h1>Posts</h1>
  <div class="wrapper">
    <ul v-if="data">
      <li v-for="post in data" :key="post.id">
        <h2>{{ post.title }}</h2>
        <div>{{ post.body }}</div>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { useQuery } from "@tanstack/vue-query";

useHead({
  title: "какой то тайтл2",
});

const fetcher = async () =>
  await fetch("https://jsonplaceholder.typicode.com/posts").then((response) =>
    response.json()
  );

const { data, suspense } = useQuery({
  queryKey: ["test"],
  queryFn: fetcher,
});

await suspense();
</script>
