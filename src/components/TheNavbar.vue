<template>
  <header class="text-gray-600 body-font">
    <div class="flex justify-between p-5 w-full">
      <div class="flex text-2xl text-gray-900 font-bold">
        <span class="text-[#ff2a7e]">Just</span><span>Shop</span>
      </div>
      <nav class="hidden md:flex text-base leading-9">
        <a class="mr-5 hover:text-gray-900">
          <RouterLink to="/">Home</RouterLink>
        </a>
        <a class="hover:text-gray-900">
          <RouterLink to="/categories">Categories</RouterLink>
        </a>
      </nav>
      <button
        class="inline-flex items-center hover:bg-gray-100 border-0 py-1 px-3 focus:outline-none rounded text-base"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          fill="currentColor"
          class="bi bi-cart"
          viewBox="0 0 16 16"
          id="IconChangeColor"
        >
          <path
            d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5zM3.102 4l1.313 7h8.17l1.313-7H3.102zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2zm7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"
            id="mainIconPathAttribute"
          ></path>
        </svg>
      </button>
    </div>
  </header>
</template>

<script setup>
import { RouterLink } from "vue-router";
</script>

<style scoped></style>
