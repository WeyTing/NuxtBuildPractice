<template>
  <h1>商品{{ productId }}</h1>
  <div class="flex gap-4">
    <p class="border p-4 mb-4 rounded-lg">
      <img :src="product.image" alt="" />
    </p>
    <div class="flex flex-col gap-4 w-1/2">
      <p class="p-4 mb-4 rounded-lg text-3xl">{{ product.title }}</p>
      <p class="p-4 mb-4 rounded-lg">{{ product.description }}</p>
      <p class="p-4 mb-4">
        <Icon name="clarity:dollar-solid" />{{ product.price }}
      </p>
      <button class="p-4 mb-4 rounded-lg bg-green-400 w-1/4 cursor-pointer">
        <Icon name="clarity:shopping-cart-solid-badged" />
        加入購物車
      </button>
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
const productId = route.params.id;

const { data } = await useFetch(
  "https://fakestoreapi.com/products" + `/${productId}`
);
const product = data.value;
</script>
