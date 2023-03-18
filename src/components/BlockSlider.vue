<template>
  <div class="bg-purple text-white rounded-borders">
    <q-carousel
      v-model="slide"
      swipeable
      animated
      :padding="padding"
      :vertical="vertical"
      :arrows="arrows"
      :navigation="navigation"
      height="300px"
      class="bg-purple text-white rounded-borders"
    >
      <q-carousel-slide
        v-for="item, key in items"
        :key="key"
        :name="`slide-${key}`"
        class="column no-wrap flex-center"
      >
        <div class="text-h1">{{ item.text }}</div>
      </q-carousel-slide>
      <!-- <q-carousel-slide name="style" class="column no-wrap flex-center">
        <q-icon name="style" size="56px" />
        <div class="q-mt-md text-center">
          {{ lorem }}
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="tv" class="column no-wrap flex-center">
        <q-icon name="live_tv" size="56px" />
        <div class="q-mt-md text-center">
          {{ lorem }}
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="layers" class="column no-wrap flex-center">
        <q-icon name="layers" size="56px" />
        <div class="q-mt-md text-center">
          {{ lorem }}
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="map" class="column no-wrap flex-center">
        <q-icon name="terrain" size="56px" />
        <div class="q-mt-md text-center">
          {{ lorem }}
        </div>
      </q-carousel-slide> -->
    </q-carousel>

    <q-btn
      flat
      dense
      icon="Mouse"
      aria-label="Mouse"
    />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

export interface BlockSliderItem {
  text?: string
}

export interface IBlockSlider {
  arrows?: boolean,
  navigation?: boolean,
  vertical?: boolean,
  padding?: boolean,
  items: BlockSliderItem[]
}

withDefaults(defineProps<IBlockSlider>(), {
  arrows: true,
  navigation: false,
  vertical: false,
  padding: false,
  items: () => []
})

const slide = ref('slide-0')

</script>