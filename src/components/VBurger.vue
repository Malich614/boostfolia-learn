<template>
  <q-btn
    flat
    dense
    icon="menu"
    aria-label="Menu"
  >
    <q-menu>
      <q-list style="min-width: 100px">
        <q-item
          v-for="item, key in menu"
          :key="key"
          v-close-popup
          clickable
        >
          <q-item-section>{{ item.text }}</q-item-section>
        </q-item>
        <!-- <q-item clickable v-close-popup>
          <q-item-section>New tab</q-item-section>
        </q-item>
        <q-item clickable v-close-popup>
          <q-item-section>New incognito tab</q-item-section>
        </q-item>
        <q-separator />
        <q-item clickable v-close-popup>
          <q-item-section>Recent tabs</q-item-section>
        </q-item>
        <q-item clickable v-close-popup>
          <q-item-section>History</q-item-section>
        </q-item>
        <q-item clickable v-close-popup>
          <q-item-section>Downloads</q-item-section>
        </q-item>
        <q-separator />
        <q-item clickable v-close-popup>
          <q-item-section>Settings</q-item-section>
        </q-item>
        <q-separator />
        <q-item clickable v-close-popup>
          <q-item-section>Help &amp; Feedback</q-item-section>
        </q-item> -->
      </q-list>
    </q-menu>
  </q-btn>
</template>

<script setup lang="ts">
import { IMenuItem } from 'src/components/models'

export interface IVBurger {
  menu?: IMenuItem[]
}

withDefaults(defineProps<IVBurger>(), {
  menu: () => []
})

</script>
