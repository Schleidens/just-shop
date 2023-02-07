<template>
  <section class="text-gray-600 body-font h-3/6 mt-5 px-5 md:px-16">
    <div
      class="rounded-3xl flex flex-col px-5 md:px-20 py-10 md:flex-row-reverse items-center bg-[#ffcbd9]"
    >
      <div class="w-full flex mb-10 items-center justify-center md:mb-0">
        <img
          class="object-center h-full w-full md:w-[62%] min-w-[52%] rounded-lg"
          :alt="title"
          :src="image"
        />
      </div>
      <div class="lg:flex-grow flex flex-col md:items-start text-left">
        <a :href="/product/ + link">
          <h1
            class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900"
          >
            {{ title }}
          </h1></a
        >
        <p class="mb-8 leading-relaxed">
          {{ description }}
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  image: String,
  link: Number,
});
</script>
