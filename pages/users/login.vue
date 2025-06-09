<template>
  <h1>登入</h1>
  <div class="flex flex-col gap-4 w-1/4">
    <div class="flex flex-col gap-2">
      <label for="username">帳號</label>
      <input
        type="text"
        placeholder="帳號"
        v-model="username"
        id="username"
        class="border p-2"
      />
    </div>
    <div class="flex flex-col gap-2">
      <label for="password">密碼</label>
      <input
        type="password"
        placeholder="密碼"
        v-model="password"
        id="password"
        class="border p-2"
      />
    </div>
    <button class="bg-green-600 px-4 py-2 text-pink-50">登入</button>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "user",
});

const username = ref("");
const password = ref("");
</script>
