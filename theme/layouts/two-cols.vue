<template>
  <div class="bg-main slidev-layout h-full">
    <div class="grid grid-cols-2 gap-16 h-full items-center px-16 py-12">
      <!-- Left Column -->
      <div class="flex justify-center items-center">
        <slot />
      </div>
      
      <!-- Right Column -->
      <div class="flex flex-col justify-center">
        <slot name="right" />
      </div>
    </div>
    
    <LayoutFooter
      :website="website"
      :hide-logo-in-corner="hideLogoInCorner"
    />
  </div>
</template>

<script setup lang="ts">
import LayoutFooter from '../components/LayoutFooter.vue'

defineProps({
  heading: {
    type: String,
  },
  website: {
    type: String,
  },
  hideLogoInCorner: {
    type: Boolean,
  },
})
</script>