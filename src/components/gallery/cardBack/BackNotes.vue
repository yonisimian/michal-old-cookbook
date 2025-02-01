<template>
  <div>
    <p class="font-general-semibold text-xl dark:text-ternary-light font-semibold mb-2">הערות</p>
    <p class="text-sm">
      {{ notes }}
    </p>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  notes: string
}>()
</script>

<style scoped></style>
