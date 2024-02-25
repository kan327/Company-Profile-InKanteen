<script setup>
const props = defineProps({
  image: String,
  title: String,
  desc: String,
})
</script>

<template>
  <div class=" relative rounded-xl overflow-hidden w-[528px] h-[283px] hover:opacity-100">
    
    <div class="text-white flex flex-col justify-end absolute inset-0  bg-gradient-to-t from-3A4 to-transparent opacity-0 hover:opacity-100 transition-opacity duration-500">
      <div class="-rotate-[5deg] mx-5 ml-10 mb-12">
        <div class="font-clash_display text-2xl uppercase font-bold">{{ title }}</div>
        <div class="font-medium line-clamp-3">{{ desc }}</div>
      </div>
    </div>
    <img :src="image" width="528" height="283" alt="">
  </div>
</template>