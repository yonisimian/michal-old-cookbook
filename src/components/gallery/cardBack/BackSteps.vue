<template>
  <div class="row-span-1 text-right px-4">
    <p class="font-general-semibold text-xl dark:text-ternary-light font-semibold">הכנה</p>
    <ul class="list-decimal list-inside text-right">
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
