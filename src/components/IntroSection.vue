<template>
  <IntroSectionComponent
    :title="product.title"
    :description="product.description"
    :image="product.image"
  />
</template>

<script setup>
import { ref, onMounted } from "vue";
import axios from "axios";

import IntroSectionComponent from "./IntroSectionComponent.vue";

const product = ref([]);
const baseUrl = "https://fakestoreapi.com/products/";
const randomProductNumber = Math.floor(Math.random() * 20);

onMounted(() => {
  getProduct();
});

const getProduct = () => {
  axios.get(baseUrl + randomProductNumber).then((response) => {
    product.value = response.data;
  });
};
</script>

<style scoped></style>
