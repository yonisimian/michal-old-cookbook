<template>
  <button
    @click="toggleDark()"
    class="text-cyan-700 hover:text-cyan-500"
    :title="isDark ? 'יהי אור' : 'יהי חושך'"
  >
    <span>{{ isDark ? '☀️' : '🌙' }}</span>
  </button>
</template>

<script setup lang="ts">
import { useTheme } from '/@/composables'

const { toggleDark, isDark } = useTheme()
</script>

<style scoped></style>
