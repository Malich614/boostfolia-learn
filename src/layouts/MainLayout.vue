<template>
  <q-layout view="hHh lpR fFf">
    <VHeader title="BOOSTFOLIA" :burger-menu="burgerMenu" />
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { IMenuItem } from 'src/components/models';
import VHeader from 'src/components/VHeader.vue';

// const burgerMenu: IMenuItem[] = [
//   {
//     text: 'Test 1'
//   },
//   {
//     text: 'Test 2'
//   }
// ]

const burgerMenu = <IMenuItem[]>[
  {
    text: 'Test 1'
  },
  {
    text: 'Test 2'
  }
]

</script>
