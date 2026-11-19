<script setup lang="ts">
useHead({ title: 'About' })
</script>

<template>
  <div>
    <h1 class="text-3xl font-extrabold tracking-wide uppercase md:text-4xl">About</h1>
    <p class="mt-3 max-w-md text-muted">What this website is for, and how it is built.</p>

    <div class="mt-10 grid gap-5 sm:grid-cols-2">
      <InfoCard
        class="bg-navy/65"
        title="Purpose"
        description="This site demonstrates component-based development. The same header, footer, and cards are reused across multiple pages."
      />
      <InfoCard
        class="bg-navy/65"
        title="How It Works"
        description="Student details are passed to StudentCard as props, so one component can display every student."
      />
      <InfoCard
        class="bg-navy/65"
        title="Our School"
        description="Caraga State University is located in Butuan City, Philippines."
      />
      <InfoCard
        class="bg-navy/65"
        title="The Courses"
        description="BS Information Technology, BS Information System, and BS Computer Science."
      />
    </div>

    <div class="mt-12">
      <AppButton label="Contact Us" color="green" />
    </div>
  </div>
</template>