<template>
  <ul class="list-none p-0 grid grid-cols-4 gap-4">
    <li
      v-for="product in productList"
      class="border p-4 mb-4 rounded-lg relative"
    >
      <ProductCard :product="product" />
    </li>
  </ul>
</template>

<script setup>
const productList = ref([]);

const { data } = await useFetch("https://fakestoreapi.com/products");
productList.value = data.value;
</script>
