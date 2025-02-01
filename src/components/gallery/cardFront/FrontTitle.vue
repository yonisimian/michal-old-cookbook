<template>
  <div class="row-span-1 text-center px-4 py-6">
    <p class="font-general-semibold text-xl dark:text-ternary-light font-semibold mb-2">
      {{ title }}
    </p>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string
}>()
</script>

<style scoped></style>
