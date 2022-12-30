<template>
  <NuxtLink :to="to"
    class="px-6 hover:bg-slate-100 flex text-center justify-center flex-col"
    active-class="text-blue-600">
      <slot />
  </NuxtLink>
</template>

<script setup lang="ts">
import type { RouteLocationRaw } from 'vue-router';

const props = defineProps<{
  to?: string | RouteLocationRaw
}>()

// setup code
</script>