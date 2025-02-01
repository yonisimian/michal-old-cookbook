<template>
  <FrontCard data-aos="fade-zoom-in">
    <FrontTitle :title="recipe.title" />
  </FrontCard>
</template>

<script setup lang="ts">
import { Recipe } from '/@/types/types'

defineProps<{
  recipe: Recipe
}>()
</script>

<style scoped></style>
