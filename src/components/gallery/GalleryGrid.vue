<template>
  <section class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 mt-6 gap-4">
    <TransitionGroup name="backCard">
      <GalleryCard
        v-for="(recipe, index) in recipes"
        :key="index"
        :id="`${recipe.title.toLowerCase().replace(/ /g, '-')}`"
        :recipe
      />
    </TransitionGroup>
  </section>
</template>

<script setup lang="ts">
import { Recipe } from '/@/types/types'

defineProps<{
  recipes: Recipe[]
}>()
</script>

<style scoped></style>
