<script setup lang="ts">
import { computed } from 'vue'
// @ts-ignore
import { isDark } from '@slidev/client/logic/dark.ts'

defineProps({
  website: {
    type: String,
  },
  hideLogoInCorner: {
    type: Boolean
  }
})

const logoImgPrefix = computed(() => isDark.value ? 'white' : 'black')
</script>

<template>
  <footer class="absolute bottom-0 left-0 w-full z-10">
    <div class="flex justify-between w-full px-4 py-1">
      <span class="font-medium text-sm" style="color: rgb(255, 107, 237);">alexop.dev</span>
      <span class="text-sm" style="color: rgb(234, 237, 243);">{{ $slidev.nav.currentPage }}</span>
    </div>
  </footer>
</template>