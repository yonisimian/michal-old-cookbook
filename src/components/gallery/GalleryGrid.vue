<template>
  <section class="flex flex-col mt-6 sm:gap-5">
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
