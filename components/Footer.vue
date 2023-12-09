<template>
  <footer class="relative border-t border-gray-200">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="flex flex-col items-start justify-between gap-y-12 pb-6 pt-16 lg:flex-row lg:items-center lg:py-16">
        <div>
          <div class="flex items-center text-gray-900"><svg viewBox="0 0 40 40" aria-hidden="true"
              class="h-10 w-10 flex-none fill-cyan-500">
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M20 40C8.954 40 0 31.046 0 20S8.954 0 20 0s20 8.954 20 20-8.954 20-20 20ZM4 20c0 7.264 5.163 13.321 12.02 14.704C17.642 35.03 19 33.657 19 32V8c0-1.657-1.357-3.031-2.98-2.704C9.162 6.68 4 12.736 4 20Z">
              </path>
            </svg>
            <div class="ml-4">
              <p class="text-base font-semibold">{{ appConfig.app_name }}</p>
              <p class="mt-1 text-sm">Invest at the perfect time.</p>
            </div>
          </div>
          <nav class="mt-11 flex gap-8">
            <!-- <a
              class="relative -mx-3 -my-2 rounded-lg px-3 py-2 text-sm text-gray-700 transition-colors delay-150 hover:text-gray-900 hover:delay-0"
              href="/#features"><span class="relative z-10">Features</span></a><a
              class="relative -mx-3 -my-2 rounded-lg px-3 py-2 text-sm text-gray-700 transition-colors delay-150 hover:text-gray-900 hover:delay-0"
              href="/#reviews"><span class="relative z-10">Reviews</span></a><a
              class="relative -mx-3 -my-2 rounded-lg px-3 py-2 text-sm text-gray-700 transition-colors delay-150 hover:text-gray-900 hover:delay-0"
              href="/#pricing"><span class="relative z-10">Pricing</span></a><a
              class="relative -mx-3 -my-2 rounded-lg px-3 py-2 text-sm text-gray-700 transition-colors delay-150 hover:text-gray-900 hover:delay-0"
              href="/#faqs"><span class="relative z-10">FAQs</span></a> -->
            <NuxtLink v-for="link in links" :to="`#${link.path}`">
              {{ link.name }}
            </NuxtLink>
          </nav>
        </div>
        <div
          class="group relative -mx-4 flex items-center self-stretch p-4 transition-colors hover:bg-gray-100 sm:self-auto sm:rounded-2xl lg:mx-0 lg:self-auto lg:p-6">
          <div class="relative flex h-24 w-24 flex-none items-center justify-center">
            <svg viewBox="0 0 96 96" fill="none" aria-hidden="true"
              class="absolute inset-0 h-full w-full stroke-gray-300 transition-colors group-hover:stroke-cyan-500">
              <path d="M1 17V9a8 8 0 0 1 8-8h8M95 17V9a8 8 0 0 0-8-8h-8M1 79v8a8 8 0 0 0 8 8h8M95 79v8a8 8 0 0 1-8 8h-8"
                stroke-width="2" stroke-linecap="round"></path>
            </svg>
            <vue-qrcode :value="appConfig.stores.apple" type="image/png"
              :color="{ dark: '#333333ff', light: '#ffffff00' }" :margin="4" />
          </div>
          <div class="ml-8 lg:w-64">
            <p class="text-base font-semibold text-gray-900"><a :href="appConfig.stores.apple" target="_blank"><span
                  class="absolute inset-0 sm:rounded-2xl"></span>Download the app</a></p>
            <p class="mt-1 text-sm text-gray-700">Scan the QR code to download the app from the App Store.</p>
          </div>
        </div>
      </div>

      <div
        class="flex flex-col items-center border-t border-gray-200 pb-12 pt-8 md:flex-row-reverse md:justify-between md:pt-6">

        <form class="flex w-full justify-center md:w-auto">
          join our newsletter
          <div class="w-60 min-w-0 shrink"><input id=":S5:" type="email" aria-label="Email address"
              placeholder="Email address" autocomplete="email" required=""
              class="block w-full appearance-none rounded-lg border border-gray-200 bg-white py-[calc(theme(spacing.2)-1px)] px-[calc(theme(spacing.3)-1px)] text-gray-900 placeholder:text-gray-400 focus:border-cyan-500 focus:outline-none focus:ring-cyan-500 sm:text-sm">
          </div><button
            class="inline-flex justify-center rounded-lg py-2 px-3 text-sm font-semibold outline-2 outline-offset-2 transition-colors relative overflow-hidden bg-cyan-500 text-white before:absolute before:inset-0 active:before:bg-transparent hover:before:bg-white/10 active:bg-cyan-600 active:text-white/80 before:transition-colors ml-4 flex-none"
            type="submit"><span class="hidden lg:inline">Join our newsletter</span><span class="lg:hidden">Join
              newsletter</span></button>
        </form>

        <p class="mt-6 text-sm text-gray-500 md:mt-0">
          <slot name="left"></slot>
        </p>
      </div>



    </div>
  </footer>
</template>

<script setup>
import VueQrcode from 'vue-qrcode';

const appConfig = useAppConfig();

defineProps(['links']);
</script>