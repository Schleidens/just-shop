<template>
  <div class="md:flex-[1_0_21%] mx-2 my-2 p-2 bg-gray-100 rounded-lg">
    <a :href="/product/ + link">
      <img class="w-full md:h-64 rounded-lg" :src="image" :alt="title" />
    </a>
    <div class="text-sm">
      <span class="font-light">{{ title }}</span>
      <br />
      <span class="font-bold">{{ price }} $</span>
    </div>
  </div>
</template>

<script setup>
defineProps({
  image: String,
  price: Number,
  title: String,
  link: Number,
});
</script>

<style scoped></style>
