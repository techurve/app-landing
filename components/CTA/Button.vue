<template>
  <div>
    <!-- {{ headers.user_agent }} -->
    <StoreApple v-if="user_agent['user-agent']?.includes('Mac')" />
    <StoreGoogle v-else />
  </div>
</template>

<script setup lang="ts">
const user_agent = useRequestHeaders(['user-agent']);
</script>