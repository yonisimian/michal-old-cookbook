<template>
  <section
    class="flex flex-col justify-between border-b border-primary-light dark:border-secondary-dark pb-3 gap-3 text-xs"
  >
    <SearchInput :filterSearch />
  </section>
</template>

<script setup lang="ts">
defineProps<{
  filterSearch: (filter: string) => void
}>()
</script>

<style scoped>
@media (min-width: 432px) {
  section {
    @apply text-base;
  }
}
@media (min-width: 684px) {
  section {
    @apply flex-row;
  }
}
</style>
