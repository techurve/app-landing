<template>
  <div class="flex flex-col items-center justify-center">
    <h2 class="text-4xl font-bold text-gray-600">{{ title }}</h2>
    <div class="flex gap-5 mt-10 text-gray-400">
      <Icon size="60" v-for="icon in icons" :name="icon" />
    </div>
  </div>
</template>

<script setup>
const props = defineProps(['title', 'icons'])
</script>