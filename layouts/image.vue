<script setup lang="ts">
  import { computed } from 'vue'
  import { handleBackground } from '@slidev/client/layoutHelper.ts'

  const props = defineProps<{
    image?: string
    position?: "top" | "center" | "bottom"
    imageBw?: boolean // black and white
  }>()

  const style = computed(() => handleBackground(props.image, false, "cover"))
  const position = computed(() => {
    switch (props.position) {
      case "top":
        return "image-top"
      case "center":
        return "image-center"
      case "bottom":
        return "image-bottom"
      default:
        return "image-top"
    }
  })
  const blackAndWhite = computed(() => props.imageBw ? "filter: grayscale(1)" : "")
</script>

<template>
  <div class="slidev-layout image" :class="position" :style="[style, blackAndWhite]">
    <div class="flex justify-center w-2/3 mx-auto">
      <slot />
    </div>
  </div>
</template>