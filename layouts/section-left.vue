<script setup lang="ts">
  import { computed } from 'vue'
  import { handleBackground } from '@slidev/client/layoutHelper.ts'

  const props = defineProps<{
    image?: string
  }>()

  const style = computed(() => handleBackground(props.image, false, "cover"))
</script>

<template>
  <div class="slidev-layout section-left" :style="style">
    <div class="my-auto h-full flex flex-col justify-center">
      <div class="box py-8 w-2/3">
        <slot />
      </div>
    </div>
  </div>
</template>