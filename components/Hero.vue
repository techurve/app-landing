<template>
  <div id="hero" class="relative isolate overflow-hidden bg-white">
    <!-- <svg
      class="absolute inset-0 -z-10 h-full w-full stroke-gray-200 [mask-image:radial-gradient(100%_100%_at_top_right,white,transparent)]"
      aria-hidden="true">
      <defs>
        <pattern id="0787a7c5-978c-4f66-83c7-11c213f99cb7" width="200" height="200" x="50%" y="-1"
          patternUnits="userSpaceOnUse">
          <path d="M.5 200V.5H200" fill="none" />
        </pattern>
      </defs>
      <rect width="100%" height="100%" stroke-width="0" fill="url(#0787a7c5-978c-4f66-83c7-11c213f99cb7)" />
    </svg> -->
    <div class="mx-auto max-w-7xl px-6 pb-24 pt-10 sm:pb-32 lg:flex lg:px-8 lg:py-40">
      <div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-xl lg:flex-shrink-0 lg:pt-8">
        <img class="h-16" src="/take_break.png" alt="Your Company" />
        <div class="mt-20 sm:mt-28 lg:mt-10">
          <NuxtLink href="/releases" class="inline-flex space-x-6">
            <span
              class="rounded-full bg-primary-600/10 px-3 py-1 text-sm font-semibold leading-6 text-primary-600 ring-1 ring-inset ring-primary-600/10">What's
              new</span>
            <span class="inline-flex items-center space-x-2 text-sm font-medium leading-6 text-gray-600">
              <span>Just shipped v1.0</span>
              <Icon name="pajamas:chevron-right" class="h-5 w-5 text-gray-400" aria-hidden="true" />
            </span>
          </NuxtLink>
        </div>
        <h1 class="mt-10 text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl">
          {{ title }}
        </h1>
        <p class="mt-6 text-lg leading-8 text-gray-600">
          {{ description }}
        </p>
        <div class="mt-10 flex items-center gap-x-6">
          <StoreApple />
          <StoreGoogle />
        </div>
      </div>
      <div class="mx-auto mt-16 flex max-w-2xl sm:mt-24 lg:ml-10 lg:mr-0 lg:mt-0 lg:max-w-none lg:flex-none xl:ml-32">
        <div class="max-w-3xl flex-none sm:max-w-5xl lg:max-w-none">
          <div>
            <img src="/take_a_break.png" alt="App screenshot" class="w-72" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

defineProps(['title', 'description'])
</script>