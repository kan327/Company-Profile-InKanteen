<script setup>
const rollimgprops = defineProps({
  time: { type: String, required: true },
  direct: { type: String, required: true}
});
</script>
<template>
      <div class="imgBox mx-auto" :class="[direct == 'R' ? 'scroll' : 'Lscroll' ]"  :style="{ '--time': time }">
        <div class="roll">
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
        </div>
        <div class="roll">
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
          <div class="w-28 h-28 md:w-52 md:h-52 flex items-center justify-center">
            <img src="https://placehold.co/200" class="object-fill" alt="">
          </div>
        </div>
      </div>
</template>
