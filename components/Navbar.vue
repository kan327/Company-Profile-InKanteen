<script setup>
let menustats = ref(false)
</script>

<template>
  <nav class="text-3A4 z-50 md:mt-5 w-full fixed top-0">
    <div class="flex justify-between px-10 py-1 items-center shadow-sha md:rounded-full md:mx-16 lg:mx-20 bg-white">
      <img src="/images/H-Logo.png" width="131" height="32" alt="">

      <div class="justify-center gap-4 -translate-x-1/4 hidden md:flex">
        <NuxtLink to="/">
          <div class="">Home</div>
        </NuxtLink>
        <NuxtLink to="/posts">
          <div>Blog</div>
        </NuxtLink>
        <NuxtLink to="/story">
          <div>Story</div>
        </NuxtLink>
        <NuxtLink to="/about-us">
          <div>About Us</div>
        </NuxtLink>
      </div>
      <div class="text-32C hidden md:block">Masuk</div>
      <div class="block md:hidden" @click="menustats = !menustats">
        <Icon name="material-symbols-light:menu-rounded" size="24" />
      </div>

    </div>
    <div v-if="menustats"
      class="flex text-end bg-white shadow-sha rounded-lg -translate-y-2 p-5 flex-col absolute -right-7 justify-center gap-4 -translate-x-1/3 md:hidden">
      <NuxtLink to="/">
        <div class="">Home</div>
      </NuxtLink>
      <NuxtLink to="/posts">
          <div>Blog</div>
        </NuxtLink>
        <NuxtLink to="/story">
          <div>Story</div>
        </NuxtLink>
      <NuxtLink to="/about-us">
        <div>About Us</div>
      </NuxtLink>
    </div>
  </nav>
</template>
