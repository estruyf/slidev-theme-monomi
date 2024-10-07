<script setup lang="ts">
  import { computed } from 'vue'

  const props = defineProps<{
    invert?: boolean
  }>()

  const invertClass = computed(() => props.invert ? "inverted" : "")
</script>

<template>
  <div class="slidev-layout default" :class="invertClass">
    <slot />
  </div>
</template>
