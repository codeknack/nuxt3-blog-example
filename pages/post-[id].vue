<script>
  export default {
    layout: "blog"
  }
</script>

<script setup>
  const route = useRoute()
  const { data: post } = await useFetch(`https://jsonplaceholder.typicode.com/posts/${route.params.id}`, { pick: ['title', 'body'] })
</script>

<template>
  <div>
    <NuxtLink to="/">
      <h1 class="m-4 hover:underline">Back to Home</h1>
    </NuxtLink>
    <quote />
    <article class="m-4 md:w-1/2 lg:w-1/3">
      <h1 class="mb-2 capitalize text-2xl font-semibold">{{ post.title }}</h1>
      <p>{{ post.body }}</p>
    </article>
  </div>
</template>
