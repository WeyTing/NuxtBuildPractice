<template>
  <div>
    <nav class="flex gap-4 p-4 shadow-md bg-white">
      <ul
        class="flex gap-4 list-none items-center justify-center w-full md:w-auto md:flex-row flex-col text-center"
      >
        <li class="hover:text-pink-500">
          <NuxtLink to="/">首頁</NuxtLink>
        </li>
        <li class="hover:text-pink-500">
          <NuxtLink to="/users/login">登入</NuxtLink>
        </li>
      </ul>
    </nav>
    <div class="container mx-auto p-4">
      <NuxtPage />
    </div>
  </div>
</template>
