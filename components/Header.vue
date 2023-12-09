<template>
  <header
    class="border-b border-gray-200 dark:border-gray-800 -mb-px sticky top-0 z-50 lg:border-b-0 lg:top-4 lg:mb-8 backdrop-blur-none bg-transparent lg:mx-4">
    <div
      class="mx-auto px-4 sm:px-6 lg:px-8 max-w-7xl flex items-center justify-between gap-3 h-16 lg:rounded-full bg-white border">
      <div class="lg:flex-1 flex items-center gap-1.5">
        <NuxtLink to="#hero" class="flex-shrink-0 font-bold text-xl text-gray-700 dark:text-white flex items-end gap-1.5">
          <slot name="logo" />
        </NuxtLink>
      </div>
      <ul class="items-center gap-x-8 hidden lg:flex">
        <li v-for="nav in navigation">
          <NuxtLink :href="`/#${nav.path}`" class="text-sm/6 font-semibold flex items-center gap-1 transition-colors"
            :class="active(nav) ? 'text-primary' : 'hover:text-primary'">
            {{ nav.name }}
          </NuxtLink>
        </li>
      </ul>
      <div class="flex items-center justify-end lg:flex-1 gap-1.5">
        <slot name="right" />

      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
interface NavigationItem {
  name: string,
  path: string,
}

const route = useRoute();

const navigation: Array<NavigationItem> = [
  { name: "Features", path: "features" },
  { name: "Testimonials", path: "testimonials" },
  { name: "Pricing", path: "pricing" },
  { name: "FAQ", path: "faq" }
];

const active = (nav: NavigationItem): boolean => route.hash === ('#' + nav.path);
</script>