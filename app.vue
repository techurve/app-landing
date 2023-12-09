<template>
  <Header :links="navigation">
    <template #logo>
      <span>{{ appConfig.app_name }}</span>
      <UBadge label="App" variant="subtle" class="mb-0.5" />
    </template>
  </Header>

  <main class="min-h-[calc(100vh-var(4rem))]">
    <NuxtPage />
  </main>

  <Footer :links="navigation">
    <template #left>
      Copyright © {{ new Date().getFullYear() }} {{ appConfig.app_name }}
    </template>
  </Footer>
</template>

<script setup lang="ts">
import { type NavigationItem } from './types/navigation_item';

const appConfig = useAppConfig();

useHead({
  title: 'App Landing Page',
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

useSeoMeta({
  description: 'Mobile app landing page template. Start converting in minutes.'
});

const navigation: Array<NavigationItem> = [
  { name: "Features", path: "features" },
  { name: "Testimonials", path: "testimonials" },
  { name: "Pricing", path: "pricing" },
  { name: "FAQ", path: "faq" }
];
</script>