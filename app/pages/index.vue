<script setup lang="ts">
useHead({ title: 'Home' })
</script>

<template>
  <div>
    <section class="pb-10">
      <p class="text-xs font-semibold tracking-[0.2em] text-muted uppercase">
        Caraga State University · Butuan City
      </p>
      <h1 class="mt-3 text-3xl font-extrabold tracking-wide uppercase md:text-4xl">
        Student Information
      </h1>
      <p class="mt-3 max-w-md text-muted">
        A simple directory of our classmates, their courses, and their year levels.
      </p>
      <div class="mt-6">
        <AppButton label="View Students" color="blue" @click="navigateTo('/students')" />
      </div>
    </section>

    <section class="grid gap-5 md:grid-cols-3">
      <InfoCard
        class="bg-sky/70"
        title="Caraga State University"
        description="Our students come from Caraga State University in Butuan City, Philippines."
      />
      <InfoCard
        class="bg-sky/70"
        title="Our Courses"
        description="BS Information Technology, BS Information System, and BS Computer Science."
      />
      <InfoCard
        class="bg-sky/70"
        title="About This Website"
        description="Built with Nuxt, Tailwind CSS, and reusable components like StudentCard, InfoCard, and AppButton."
      />
    </section>
  </div>
</template>