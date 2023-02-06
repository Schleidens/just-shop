<template>
  <section class="text-gray-600 body-font overflow-hidden">
    <div class="container px-5 md:px-36 py-24">
      <div class="mx-auto flex flex-wrap md:flex-nowrap">
        <img
          alt="ecommerce"
          class="md:w-1/2 w-full h-full object-cover object-center rounded"
          :src="image"
        />
        <div class="w-full lg:pl-10 lg:py-6 mt-6 lg:mt-0">
          <h2 class="text-sm title-font text-gray-500 tracking-widest mb-2">
            {{ categorie }}
          </h2>
          <h1 class="text-gray-900 text-3xl title-font font-medium mb-4">
            {{ title }}
          </h1>
          <p class="leading-relaxed">
            {{ description }}
          </p>
          <div class="mt-4">
            <span class="title-font text-2xl font-bold text-gray-900"
              >{{ price }}$</span
            >
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  categorie: String,
  title: String,
  description: String,
  image: String,
  price: Number,
});
</script>

<style scoped></style>
