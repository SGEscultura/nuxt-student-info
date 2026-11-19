<script setup lang="ts">
// Add or rename menu items here
const links = [
  { to: '/', label: 'Home' },
  { to: '/students', label: 'Students' },
  { to: '/about', label: 'About' },
]
</script>

<template>
  <header
    class="sticky top-0 z-40 border-b border-white/30 bg-deep/90 text-white backdrop-blur-md"
  >
    <div class="mx-auto flex max-w-5xl flex-wrap items-center justify-between gap-3 px-6 py-4">
      <NuxtLink
        to="/"
        class="text-sm font-extrabold tracking-[0.2em] uppercase focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-white"
      >
        Student Info
      </NuxtLink>

      <nav class="flex gap-1 text-xs font-semibold tracking-[0.18em] uppercase" aria-label="Main">
        <NuxtLink
          v-for="link in links"
          :key="link.to"
          :to="link.to"
          class="rounded-full px-4 py-2 text-white/80 transition hover:bg-white/15 hover:text-white focus-visible:outline-2 focus-visible:outline-white"
          exact-active-class="bg-mist! text-deep!"
        >
          {{ link.label }}
        </NuxtLink>
      </nav>
    </div>
  </header>
</template>