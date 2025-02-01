<template>
  <div class="row-span-1 text-center px-4">
    <p class="font-general-semibold text-xl dark:text-ternary-light font-semibold mb-2">הכנה</p>
    <ul class="text-right">
      <li v-for="(step, index) in steps" :key="index" class="text-sm dark:text-ternary-light">
        {{ step }}
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  steps: string[]
}>()
</script>

<style scoped></style>
