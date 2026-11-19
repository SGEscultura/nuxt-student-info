<script setup lang="ts">
defineProps<{
  title: string
  description: string
}>()
</script>

<template>
  <div class="glass rounded-3xl p-6 text-ink">
    <h3 class="text-sm font-extrabold tracking-[0.14em] uppercase">{{ title }}</h3>
    <p class="mt-2 text-sm leading-relaxed font-medium text-ink/75">{{ description }}</p>
  </div>
</template>