<script>
  export default {
    layout: "blog"
  }
</script>

<script setup>
  const { counter, increment, decrement, counterDouble } = useCounter()
</script>

<template>
  <div>
    <p class="m-2 text-3xl"><span class="font-semibold">Counter:</span> {{ counter }} x 2 = {{ counterDouble }}</p>
    <button @click="increment" class="m-2 py-2 px-4 bg-blue-500 text-white font-semibold rounded-lg shadow-md hover:bg-blue-700">+ Increment</button>
    <button @click="decrement" class="m-2 py-2 px-4 bg-blue-500 text-white font-semibold rounded-lg shadow-md hover:bg-blue-700">- Decrement</button>
  </div>
</template>