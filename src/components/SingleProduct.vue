<template>
  <SingleProductComponent
    :categorie="product.category"
    :title="product.title"
    :description="product.description"
    :image="product.image"
    :price="product.price"
  />
</template>

<script setup>
import SingleProductComponent from "./SingleProductComponent.vue";

import axios from "axios";
import { ref, onMounted } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const id = route.params.id;

const baseUrl = "https://fakestoreapi.com/products";
const product = ref([]);

onMounted(() => {
  getProduct();
});

const getProduct = () => {
  axios.get(baseUrl + "/" + id).then((response) => {
    product.value = response.data;
  });
};
</script>

<style scoped></style>
