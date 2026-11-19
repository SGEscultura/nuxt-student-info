<script setup lang="ts">
defineProps<{
  name: string
  course: string
  year: string
}>()
</script>

<template>
  <article
    class="glass rounded-3xl p-7 text-ink transition duration-300 hover:-translate-y-1"
  >
    <span class="rounded-full bg-white/55 px-3 py-1 text-[11px] font-bold tracking-[0.18em] uppercase">
      {{ year }}
    </span>
    <h3 class="mt-8 text-lg leading-snug font-extrabold tracking-wide uppercase">{{ name }}</h3>
    <p class="mt-2 text-sm font-medium text-ink/75">{{ course }}</p>
  </article>
</template>