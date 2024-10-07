<script setup lang="ts">
  import { computed } from 'vue'
  import { onSlideEnter, useNav } from '@slidev/client'

  const props = defineProps<{
    invert?: boolean
  }>()

  const invertClass = computed(() => props.invert ? "inverted" : "")

  const getContentWidth = (element: HTMLElement) => {
    const style = window.getComputedStyle(element);
    const padding = parseFloat(style.paddingLeft) + parseFloat(style.paddingRight);
    return element.clientWidth - padding;
  }

  const adjustFontSize = (heading: HTMLHeadingElement, container: HTMLElement) => {
    const desiredWidth = getContentWidth(container);
    let fontSize = parseInt(window.getComputedStyle(heading, null).getPropertyValue('font-size'));
    while (heading.scrollWidth > desiredWidth && fontSize > 0) {
      fontSize--;
      heading.style.fontSize = fontSize + 'px';
    }
  }

  const updateFontSize = (pageNr: number, retry = 0) => {
    const el = document.querySelector(`.slidev-page-${pageNr} .slidev-layout.fact h1`)
    if (!el) return

    if (el.clientWidth === 0) {
      setTimeout(() => updateFontSize(pageNr, retry + 1), 100)
      return
    }

    if (retry > 10) return

    const container = document.querySelector(`.slidev-page-${pageNr} .slidev-layout.fact`) as HTMLElement
    if (!container) return

    adjustFontSize(el as HTMLHeadingElement, container)
  }

  onSlideEnter(() => {
    const { currentPage } = useNav();
    setTimeout(() => {
      updateFontSize(currentPage.value);
    }, 0);
  })
</script>

<template>
  <div class="slidev-layout fact" :class="invertClass">
    <slot />
  </div>
</template>
