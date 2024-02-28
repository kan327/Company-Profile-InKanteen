<script setup>
import Default from '~/layouts/Default.vue'
definePageMeta({
  layout: 'Default',
});

import { useQuery } from "@tanstack/vue-query"

const fetcher = async () =>
  await fetch('http://127.0.0.1:8000/api/getAllPosts').then((response) =>
    response.json(),
  )

const { data, suspense } = useQuery({ queryKey: ['test'], queryFn: fetcher })
await suspense()
console.log("================================")
console.log(data.value.posts)
</script>
<template>
  <Default>
    <div class="grid grid-cols-3 xs:grid-cols-4 md:grid-cols-5 gap-1 mx-auto w-fit mt-32 text-xs md:text-sm">
  
      <div v-for="item in data.posts" :key="item.id">
        <div class="relative overflow-hidden min-w-[100px]">
          <div class="flex flex-col justify-end absolute inset-0">
            <div class="p-1 xs:p-3 lg:p-5 font-semibold inset-0  bg-gradient-to-t from-8B to-transparent">
              <div class="line-clamp-1 text-black">{{ item.title }}</div>
            </div>
          </div>
          <img :src="item.featured_image" width="200" height="200" class="w-full h-full object-fill" alt="">
        </div>
      </div>
  
    </div>
  </Default>
</template>