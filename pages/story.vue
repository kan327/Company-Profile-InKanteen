<script setup>
import Default from '~/layouts/Default.vue'
definePageMeta({
  layout: 'Default',
});
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
          <img src="https://placehold.co/562x299" width="562" height="299" class="object-fill w-full md:w-auto" alt="">
        </div>

        <div class="text-3A4 md:max-w-[560px]">
          <div class="mt-5 mb-4">
            <h1 class="font-medium text-xl md:text-3xl">Title Here...</h1>
            <p>#makan_bareng #any #...</p>
          </div>
          <div>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
            industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and
            scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into
            electronic typesetting, remaining essentially unchanged.</div>
        </div>
      </div>
      <div class="xs:w-fit sm:pl-4 sm:pr-0 lg:pl-5 lg:pr-5 py-5">
        <div class="text-lg leading-none">Other Story</div>

        <div class="mt-3 md:mt-11 flex flex-col gap-5 pt-1 text-3A4">
          <div class="xs:flex gap-3 items-center">
            <div class="relative overflow-hidden xs:w-fit rounded-xl">
              <div class="flex flex-col justify-end absolute inset-0">
                <div class="mt-20 px-5 py-5 font-semibold inset-0  bg-gradient-to-t from-8B to-transparent">
                </div>
              </div>
              <img src="https://placehold.co/174x93" width="174" height="93" class="object-fill w-full xs:w-32 lg:w-auto"
                alt="">
            </div>
            <div class="w-fit hidden xs:block">
              <h2 class="font-semibold text-base md:text-xl w-fit line-clamp-1">Title Here</h2>
              <p class="md:text-base md:w-32 xl:w-auto line-clamp-2">#makan_bareng #any #...</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Default>
</template>

