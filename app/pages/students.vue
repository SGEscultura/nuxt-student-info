<script setup lang="ts">
useHead({ title: 'Students' })

// Add or edit students here. Each one becomes a StudentCard.
const students = [
  { name: 'Aliah Levi Mala', course: 'BS Information Technology', year: '3rd Year' },
  { name: 'Shen Marie Magallanes', course: 'BS Information System', year: '2nd Year' },
  { name: 'Ace Nathaniel Magbanua', course: 'BS Computer Science', year: '1st Year' },
]
</script>

<template>
  <div>
    <h1 class="text-3xl font-extrabold tracking-wide uppercase md:text-4xl">Students</h1>
    <p class="mt-3 max-w-md text-muted">
      Every card is the same component, filled in with different props.
    </p>

    <div class="mt-10 grid gap-5 sm:grid-cols-2 lg:grid-cols-3">
      <StudentCard
        v-for="student in students"
        :key="student.name"
        class="bg-azure/70"
        :name="student.name"
        :course="student.course"
        :year="student.year"
      />
    </div>

    <div class="mt-12">
      <AppButton label="Back to Home" color="gray" @click="navigateTo('/')" />
    </div>
  </div>
</template>