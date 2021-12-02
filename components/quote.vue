<script setup>
  const quote = ref('')
  const { data: qotd } = await useFetch('https://favqs.com/api/qotd')
  quote.value = qotd.value.quote
</script>

<template>
  <div class="p-4 md:w-1/2 lg:w-1/3">
    <p class="p-2 font-bold bg-blue-400 text-white">Quote of the Day</p>
    <div class="p-2 bg-blue-100  text-indigo-600">
      <p class="italic">{{ quote.body }}</p> 
      <p class="mt-2 italic text-sm font-medium">- {{ quote.author }}</p>
    </div>
  </div>
</template>