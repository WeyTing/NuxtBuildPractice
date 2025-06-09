<template>
  <h3 class="text-xl mb-4 overflow-hidden text-ellipsis whitespace-nowrap">
    <NuxtLink :to="`/products/${product.id}`">{{ product.title }} </NuxtLink>
  </h3>
  <!--圖案要置中-->
  <div class="mb-4 w-[150px] h-[150px] flex relative transform translate-x-1/2">
    <img :src="product.image" alt="" class="w-full h-full" />
  </div>
  <footer class="flex justify-between">
    <span>{{ product.rating.rate }} stars</span>
    <span>{{ product.rating.count }} reviews</span>
    <span>{{ product.id }}</span>
    <span>{{ product.price }} USD</span>
  </footer>
  <button class="bg-green-600 px-4 py-2 text-pink-50 cursor-pointer rounded">
    加入購物車
  </button>
</template>

<script setup>
defineProps({
  product: {
    type: Object,
    required: true,
  },
});
</script>
