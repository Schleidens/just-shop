<template>
  <div v-if="products != 0" class="flex flex-wrap mt-5 px-5 md:px-36">
    <ProductComponent
      v-for="{ id, title, price, image } in products"
      :key="id"
      :title="title"
      :price="price"
      :image="image"
      :link="id"
    />
  </div>
  <div v-else class="flex flex-wrap mt-5 px-5 md:px-36">
    <ProductComponentSkeleton v-for="index in 8" :key="index" />
  </div>
</template>

<script setup>
import ProductComponent from "./ProductComponent.vue";
import ProductComponentSkeleton from "./skeleton/ProductComponentSkeleton.vue";

import { ref, onMounted } from "vue";
import axios from "axios";

const products = ref([]);
const baseUrl = "https://fakestoreapi.com/products";

onMounted(() => {
  getProduct();
});

const getProduct = () => {
  axios.get(baseUrl).then((response) => {
    products.value = response.data;
  });
};
</script>

<style scoped></style>
