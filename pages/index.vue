<script setup >
import Default from '~/layouts/Default.vue'
import { useWindowScroll, useScroll } from '@vueuse/core'
import { onBeforeMount, onMounted, onUpdated, ref } from "vue"
definePageMeta({
  layout: 'Default',
});

const items = [
  {
    id: 1,
    img: "https://placehold.co/528x283",
    title: "Cara Baru Jajan Dikantin",
    desc: "Lorem Ipsum is simply dummy text of the printing and typesetting industry."
  },
  {
    id: 2,
    img: "https://placehold.co/528x283",
    title: "Cara Baru Jajan Dikantin",
    desc: "Lorem Ipsum is simply dummy text of the printing and typesetting industry."
  },
  {
    id: 3,
    img: "https://placehold.co/528x283",
    title: "Cara Baru Jajan Dikantin",
    desc: "Lorem Ipsum is simply dummy text of the printing and typesetting industry."
  },
  {
    id: 4,
    img: "https://placehold.co/528x283",
    title: "Cara Baru Jajan Dikantin",
    desc: "Lorem Ipsum is simply dummy text of the printing and typesetting industry."
  },
]

let { y: YContainer } = useWindowScroll()

let scrollContainer = ref(null)
let { x, y } = useScroll(scrollContainer)

watchEffect(() => {
  console.log(scrollContainer.value)
  // scrollContainer.value.scrollLeft += 100
})

</script>

<template>
  <Default>
    <div class="sm:h-screen relative w-[100vw] overflow-clip flex flex-col-reverse sm:flex-row justify-between">
      <div
        class="w-[225%] -z-10 -translate-y-20 absolute bg-3A4 h-screen rotate-[30deg] -translate-x-[5%] hidden lg:block">
      </div>
      <!-- <img src="/images/Hero-Image.png" class="w-full block sm:hidden mt-20" alt=""> -->

      <div class="text-center sm:text-left sm:w-fit sm:self-center sm:ml-5 lg:ml-20 md:ml-16">
        <div class="uppercase text-32C text-4xl sm:text-5xl xl:text-7.5xl leading-none font-clash_display font-bold">
          INKANTEEN</div>
        <div class="mx-auto sm:mx-0 w-5/6 sm:w-[340px] xl:w-[435px] mb-5 mt-2">Lorem Ipsum is simply dummy text
          of the printing and typesetting industry
          Lorem Ipsum
          has been the industrys standard dummy text ever since the 1500s</div>
        <button class="bg-32C text-white px-5 py-2 rounded-lg font-semibold">visit web</button>
      </div>

      <div class="flex items-center overflow-hidden flex-1">
        <div>
          <img src="/images/Hero-Image.png" class="md:relative md:-translate-y-24 mt-32 sm:mt-0 sm:block" alt="">
        </div>
      </div>
    </div>
    <!-- <div class="p-5 relative -top-12 mx-auto border-3A4 border-2 border-solid w-fit rounded-lg rotate-45">
      <div class="-rotate-45">
        <Icon name="ep:arrow-down-bold" size="20" color="#3A4064" />
      </div>
    </div> -->
    <!-- <div class="overflow-x-hidden h-screen pt-32 -mt-10">
      <div class="flex gap-3 rotate-[10deg]" ref="scrollContainer">
        <div v-for="item in items" :key="item.id">
          <TrailImg :image="item.img" :title="item.title" :desc="item.desc" />
        </div>
      </div>
    </div> -->

    <main class="mt-20 sm:mt-0">
      <div class="mx-5 sm:mx-16 lg:mx-20 mb-20 text-center md:text-start">
        <div class="uppercase text-32C text-4xl sm:text-5xl xl:text-7.5xl leading-none font-clash_display font-bold">
          TERPERCAYA
        </div>
        <div class="flex items-center flex-col md:flex-row">
          <div class="h-fit w-fit items-center md:items-start flex justify-center md:justify-start flex-col lg:flex-row">
            <div>
              <img src="/images/H-Logo.png" class="cursor-pointer select-none" width="240" height="103" alt="">
            </div>
            <div class="mx-auto sm:mx-0 w-5/6 mb-5 mt-2 sm:w-3/4 md:w-full lg:w-3/4 md:pr-5 text-center md:text-justify">
              Lorem Ipsum is simply dummy text of the printing
              and typesetting
              industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,
            </div>
          </div>
          <div class="w-full h-fit flex justify-end lg:-translate-y-1/4 xl:-translate-y-1/2">
            <div class="mx-auto items-end md:mx-0 grid grid-cols-4 gap-1 w-fit">
              <div class="bg-neutral-300 w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-xl"></div>
              <div class="bg-neutral-300 w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-xl"></div>
              <div class="bg-neutral-300 w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-xl"></div>
              <div class="bg-neutral-300 w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-xl"></div>
              <div class="bg-neutral-300 w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-xl"></div>
              <div class="bg-neutral-300 w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-xl"></div>
              <div class="bg-neutral-300 w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-xl"></div>
              <div class="bg-neutral-300 w-14 h-14 sm:w-16 sm:h-16 md:w-20 md:h-20 rounded-xl"></div>
            </div>
          </div>
        </div>
      </div>
      <div class="mx-auto w-fit text-3A4 text-xl mb-8">Mitra Kami</div>
      <SharedRollImg time="40s" direct="R"/>
      <SharedRollImg time="40s" direct="L"/>



      <div class="mt-36 overflow-x-clip relative text-white">
        <div class="w-[200%] -z-10 -top-10 absolute bg-32C h-[120vh] sm:h-screen rotate-[10deg] -translate-x-1/3">
        </div>
        <div class="flex flex-col md:flex-row translate-y-20 z-40">
          <div class="md:ml-5 lg:ml-20 mt-10 relative md:w-fit text-center md:text-justify">
            <div class="uppercase text-4xl sm:text-5xl xl:text-7.5xl leading-none font-clash_display font-bold">
              CONTACT US.</div>
            <div class="w-5/6 md:w-[340px] xl:w-[435px] mb-4 mx-auto md:mx-0">Lorem Ipsum is simply dummy
              text of the
              printing and typesetting
              industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.
            </div>
            <ul class="font-semibold text-base gap-1.5 hidden md:block">
              <li>inkanteen@info.co</li>
              <li>+62 89120004271</li>
              <li class="underline">Customer Support</li>
            </ul>
          </div>
          <div class="w-full xs:w-11/12 sm:w-3/4 md:w-full mx-auto flex-1 text-5F text-base">
            <div class="relative bg-white shadow-sha rounded-t-2xl mx-6 border-32C border-dashed border-b-2">
              <div class="p-5 lg:p-9 gap-3 flex flex-col">
                <input type="text" class="text-sm p-3 lg:p-5 rounded-xl border-8B border-solid border-2 outline-3A4"
                  placeholder="Title Here" name="title" id="">
                <textarea name="memo" class="text-sm p-3 lg:p-5 rounded-xl border-8B border-solid border-2 outline-3A4"
                  placeholder="Memo Here"></textarea>
              </div>
              <div class="bg-32C w-10 h-10 lg:w-12 lg:h-12 rounded-full absolute -bottom-5 -left-5 z-10">
              </div>
            </div>
            <div class="relative bg-white shadow-sha md:rounded-b-2xl mx-6 border-32C border-dashed border-t-2">
              <div class="bg-32C w-10 h-10 lg:w-12 lg:h-12 rounded-full absolute -top-5 -right-5">
              </div>
              <div class="p-5 lg:p-9 gap-3 flex flex-col">
                <input type="text" class="text-sm p-3 lg:p-5 rounded-xl border-8B border-solid border-2 outline-3A4"
                  placeholder="Location Here" name="Location" id="">
                <input type="text" class="text-sm p-3 lg:p-5 rounded-xl border-8B border-solid border-2 outline-3A4"
                  placeholder="Your Tenant/Place Name Here" name="Tenant" id="">
                <input type="email" class="text-sm p-3 lg:p-5 rounded-xl border-8B border-solid border-2 outline-3A4"
                  placeholder="Your Email Here" name="Email" id="">
                <div class="flex justify-center md:justify-end mt-3 lg:mt-8">
                  <div class="flex cursor-pointer select-none">
                    <div class="bg-3A4 rounded-l-2xl px-4 py-3 relative border-white border-dashed border-r-[1px]">
                      <div class="bg-5F w-6 h-6"></div>
                      <div class="bg-white w-4 h-4 rounded-full absolute -top-2 -right-2 z-10">
                      </div>
                    </div>
                    <div class="bg-3A4 rounded-r-2xl px-4 py-3 relative border-white border-dashed border-l-[1px]">
                      <div class="bg-white w-4 h-4 rounded-full absolute -bottom-2 -left-2 z-10">
                      </div>
                      <div class="uppercase font-bold text-base text-white">kirim</div>
                    </div>
                  </div>
                </div>
              </div>

            </div>
            <div
              class="relative bg-white shadow-sha rounded-b-2xl mx-6 border-32C border-dashed border-t-2 text-center p-3 md:hidden">
              <div>inkanteen@info.co</div>
              <div>+62 89120004271</div>
              <div class="underline">Customer Support</div>
            </div>
          </div>
        </div>
      </div>
    </main>

    <ComFooter/>
  </Default>
</template>