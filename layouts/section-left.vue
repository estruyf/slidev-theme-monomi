<script setup lang="ts">
  import { computed } from 'vue'
  import { handleBackground } from '@slidev/client/layoutHelper.ts'

  const props = defineProps<{
    image?: string
    imageBw?: boolean // black and white
    invert?: boolean
  }>()

  const style = computed(() => handleBackground(props.image, false, "cover"))
  const blackAndWhite = computed(() => props.imageBw ? "filter: grayscale(1)" : "")
  const invertClass = computed(() => props.invert ? "inverted" : "")
</script>

<template>
  <div class="slidev-layout section-left" :class="invertClass" :style="[style, blackAndWhite]">
    <div class="my-auto h-full flex flex-col justify-center">
      <div class="box py-8 w-2/3">
        <slot />
      </div>
    </div>
  </div>
</template>