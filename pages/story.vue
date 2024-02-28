<script setup>
import Default from '~/layouts/Default.vue'
definePageMeta({
  layout: 'Default',
});

let page = ref(0)

import { useQuery } from "@tanstack/vue-query"

const fetcher = async () =>
  await fetch('http://127.0.0.1:8000/api/getAllStories').then((response) =>
    response.json(),
  )

const { data, suspense } = useQuery({ queryKey: ['test'], queryFn: fetcher })
await suspense()
console.log("================================")
console.log(data.value.posts)
</script>
<template>
  <Default>
    <div class="mx-7 lg:mx-auto md:w-fit mt-32 flex flex-col md:flex-row">
      <div class="flex-1">
        <div class="flex items-center gap-3 mb-3 md:mb-10 text-3A4">
          <img src="/images/icon.png" width="50" height="50"
            class="object-fill rounded-full border-2 border-32C border-solid" alt="">
          <div>
            <div class="text-base md:text-lg leading-none line-clamp-1">InKanteen</div>
            <div>6 Days Ago</div>
          </div>
        </div>
        <div class="relative overflow-hidden md:w-fit rounded-xl">
          <div class="flex flex-col justify-end absolute inset-0">
            <div class="mt-20 px-5 py-5 font-semibold inset-0  bg-gradient-to-t from-8B to-transparent">
            </div>
          </div>
          <img :src="data.stories[page].featured_image" width="562" height="299" class="object-fill w-full md:w-auto" alt="">
        </div>

        <div class="text-3A4 md:max-w-[560px]">
          <div class="mt-5 mb-4">
            <h1 class="font-medium text-xl md:text-3xl">{{ data.stories[page].title }}</h1>
            <p>{{ data.stories[page].tags }}</p>
          </div>
          <div>{{ data.stories[page].desc }}</div>
        </div>
      </div>
      <div class="xs:w-fit sm:pl-4 sm:pr-0 lg:pl-5 lg:pr-5 py-5">
        <div class="text-lg leading-none">Other Story</div>
        <div class="mt-3 md:mt-11 flex flex-col gap-3 pt-1 text-3A4">
          <div v-for="(item, index) in data.stories" :key="item.id">
            <div class="xs:flex gap-3 items-center cursor-pointer" @click="page = index">
              <div class="relative overflow-hidden xs:w-fit rounded-xl">
                <div class="flex flex-col justify-end absolute inset-0">
                  <div class="mt-20 px-5 py-5 font-semibold inset-0  bg-gradient-to-t from-8B to-transparent">
                  </div>
                </div>
                <img :src="item.featured_image" width="174" height="93"
                  class="object-fill xs:w-32 lg:w-auto w-[174px] h-[93px]" alt="">
              </div>
              <div class="w-fit hidden xs:block">
                <h2 class="font-semibold text-base md:text-xl w-fit max-w-52 line-clamp-1">{{ item.title }}</h2>
                <p class="md:text-base md:w-32 xl:w-auto line-clamp-2">{{ item.tags }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Default>
</template>

