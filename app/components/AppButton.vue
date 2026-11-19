<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    label: string
    color?: 'blue' | 'green' | 'gray' | 'red'
  }>(),
  { color: 'blue' },
)

// Each color name shows that color as a see-through tint
const colors = {
  blue: 'bg-[#2196f3]/45 hover:bg-[#2196f3]/65',
  green: 'bg-[#4cc38a]/50 hover:bg-[#4cc38a]/70',
  gray: 'bg-white/50 hover:bg-white/75',
  red: 'bg-[#ff6b7a]/50 hover:bg-[#ff6b7a]/70',
}
</script>

<template>
  <button
    type="button"
    class="rounded-full border border-white/70 px-6 py-2.5 text-xs font-bold tracking-[0.18em] text-ink uppercase backdrop-blur transition duration-300 focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-ink"
    :class="colors[props.color]"
  >
    {{ label }}
  </button>
</template>