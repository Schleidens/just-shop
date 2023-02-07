<template>
  <IntroSectionComponent
    v-if="product != 0"
    :title="product.title"
    :description="product.description"
    :image="product.image"
    :link="product.id"
  />
  <IntroSectionSkeleton v-else />
</template>

<script setup>
import { ref, onMounted } from "vue";
import axios from "axios";

import IntroSectionComponent from "./IntroSectionComponent.vue";
import IntroSectionSkeleton from "./skeleton/IntroSectionSkeleton.vue";

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
