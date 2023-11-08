<template>
  <h1>Posts</h1>
  <ul v-if="data" class="wrapper">
    <li v-for="post in data" :key="post.id">
      <h2>{{ post.title }}</h2>
      <div>{{ post.body }}</div>
    </li>
  </ul>
</template>

<script setup lang="ts">
import { useQuery } from "@tanstack/vue-query";

useHead({
  title: "tanstack query",
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

console.log(
  useQuery({
    queryKey: ["test"],
  })
);
</script>
