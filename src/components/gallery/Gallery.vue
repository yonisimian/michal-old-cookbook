<template>
  <main class="pt-6 sm:pt-14 pb-8 min-h-[100svh]">
    <h2 class="text-4xl font-bold mb-8 text-center">מחברת המתכונים הישנה של מיכל</h2>
    <SearchBar :filterSearch="(text: string) => searchRecipe = text" />
    <GalleryGrid :recipes="filteredRecipes" />
  </main>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'
import { Recipe } from '/@/types/types'
import recipesData from '/@/data/recipes'

const searchRecipe = ref('')
const recipes = ref<Recipe[]>(recipesData)

const filteredRecipes = computed(() => {
  let filtered = recipes.value
  if (searchRecipe.value) {
    filtered = filterRecipesBySearch(filtered)
  }
  return filtered
})

const filterRecipesBySearch = (recipes: Recipe[]) => {
  const recipe = new RegExp(searchRecipe.value, 'i')

  const deepSearch = (obj: any): boolean => {
    return Object.values(obj).some((value) => {
      if (typeof value === 'string') {
        return recipe.test(value)
      } else if (typeof value === 'object' && value !== null) {
        return deepSearch(value)
      }
      return false
    })
  }

  return recipes.filter((el) => deepSearch(el))
}
</script>

<style scoped></style>
