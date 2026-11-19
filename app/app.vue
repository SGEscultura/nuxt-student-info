<script setup lang="ts">
useHead({
  titleTemplate: (t) => (t ? `${t} | Student Information` : 'Student Information'),
  htmlAttrs: { lang: 'en' },
  link: [
    { rel: 'preconnect', href: 'https://fonts.googleapis.com' },
    { rel: 'preconnect', href: 'https://fonts.gstatic.com', crossorigin: '' },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800&display=swap',
    },
  ],
})
</script>

<template>
  <div class="flex min-h-screen flex-col">
    <AppHeader />
    <main class="mx-auto w-full max-w-5xl flex-1 px-6 pt-6 pb-16">
      <NuxtPage />
    </main>
    <AppFooter />
  </div>
</template>