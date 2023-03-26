<script setup lang="ts">
import { LOCALSTORAGE_PREFIX } from 'src/configs';
import { useLocalStorage } from '@vueuse/core';
import DashboardHeader from 'src/components/Layout/DashboardHeader/DashboardHeader.vue';
import DashboardLeftDrawer from 'components/Layout/DashboardLeftDrawer/DashboardLeftDrawer.vue';

const leftDrawerOpen = useLocalStorage(
  `${LOCALSTORAGE_PREFIX}_leftDrawer`,
  false
);

const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value;
};
</script>

<template>
  <q-layout view="lHr lpr lfr">
    <DashboardHeader @on-toggle-drawer="toggleLeftDrawer" />

    <q-drawer v-model="leftDrawerOpen" side="left">
      <DashboardLeftDrawer />
    </q-drawer>

    <q-page-container class="bg-grey-2">
      <router-view />
    </q-page-container>
  </q-layout>
</template>
