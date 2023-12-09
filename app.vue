<template>
  <Header :links="links">
    <template #logo>
      <span>{{ appConfig.app_name }}</span>
      <UBadge label="App" variant="subtle" class="mb-0.5" />
    </template>

    <template #right>
      <UColorModeButton />

      <UButton to="https://github.com/nuxt-ui-pro/starter" target="_blank" icon="i-simple-icons-github"
        aria-label="GitHub" color="gray" variant="ghost" />
    </template>
  </Header>

  <main class="min-h-[calc(100vh-var(4rem))]">
    <NuxtPage />
  </main>

  <Footer>
    <template #left>
      Copyright © {{ new Date().getFullYear() }}
    </template>
  </Footer>
</template>

<script setup>
const appConfig = useAppConfig();
const links = [{
  label: 'Features',
  to: '#features',
  exactHash: true
}, {
  label: 'Documentation',
  to: 'https://ui.nuxt.com/pro',
  target: '_blank'
}]

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
})
</script>