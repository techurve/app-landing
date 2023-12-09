<template>
  <div>
    <Hero :title="page.hero.title" :description="page.hero.description" />
    <Logos :title="page.logos.title" :icons="page.logos.icons" />
    <Features :title="page.features.title" :description="page.features.description" :items="page.features.items" />
    <Testimonials />
    <CTA />
    <Pricing />
    <FAQ />
  </div>
</template>

<script setup>
definePageMeta({
  colorMode: 'light'
})

const { data: page } = await useAsyncData('index', () => queryContent('/').findOne())

useSeoMeta({
  title: page.value.title,
  ogTitle: page.value.title,
  description: page.value.description,
  ogDescription: page.value.description,
  ogTitle: page.value.title,
  ogDescription: page.value.description,
  ogImage: '/take_a_break.png',
  twitterTitle: page.value.title,
  twitterDescription: page.value.description,
  twitterImage: '/take_a_break.png',
  twitterCard: 'summary'
});
</script> 