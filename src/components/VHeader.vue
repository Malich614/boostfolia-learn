<template>
  <q-header reveal elevated class="bg-primary text-white">
    <q-toolbar>
      <q-toolbar-title>
        {{ title }}
      </q-toolbar-title>
      <VBurger :menu="burgerMenu" />
    </q-toolbar>
  </q-header>
</template>

<script setup lang="ts">
import VBurger from 'src/components/VBurger.vue'
import { IMenuItem } from 'src/components/models'

export interface IVHeader {
  title?: string,
  burgerMenu: IMenuItem[]
}

withDefaults(defineProps<IVHeader>(), {
  title: '',
  burgerMenu: () => []
})

</script>
