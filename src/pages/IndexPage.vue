<template>
  <q-page>
    <BlockSlider :items="sliderItems" />
  </q-page>
</template>

<script setup lang="ts">
import BlockSlider, { BlockSliderItem } from 'src/components/BlockSlider.vue'

// const sliderItems = ref(<BlockSliderItem[]>[
//   {
//     text: 'WE THINK CREATIVE BE CREATIVE'
//   },
//   {
//     text: 'WE THINK CREATIVE BE CREATIVE 2'
//   },
//   {
//     text: 'WE THINK CREATIVE BE CREATIVE 3'
//   }
// ])

const sliderItems: BlockSliderItem[] = [
  {
    text: 'WE THINK CREATIVE BE CREATIVE'
  },
  {
    text: 'WE THINK CREATIVE BE CREATIVE 2'
  },
  {
    text: 'WE THINK CREATIVE BE CREATIVE 3'
  }
]
</script>
