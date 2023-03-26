<script setup lang="ts">
import styles from './DashboardHeader.module.scss';
import { ref } from 'vue';

const search = ref('');

const emit = defineEmits<{
  (e: 'on-toggle-drawer'): void;
}>();
</script>

<template>
  <q-header class="bg-white text-dark" height-hint="98">
    <q-toolbar class="q-pa-lg">
      <q-btn
        dense
        flat
        round
        icon="menu"
        @click="() => emit('on-toggle-drawer')"
      />

      <q-toolbar-title>Dashboard</q-toolbar-title>

      <q-space />

      <div class="q-gutter-lg row items-center no-wrap">
        <q-btn round dense flat color="dark" icon="notifications" size="lg">
          <q-badge color="primary" text-color="secondary" floating>
            <strong>12</strong>
          </q-badge>
          <q-tooltip>Notifications</q-tooltip>
        </q-btn>

        <q-btn round flat>
          <q-avatar size="57px">
            <img src="https://avatars.githubusercontent.com/u/24358839?v=4" />
          </q-avatar>
          <q-tooltip>Account</q-tooltip>
        </q-btn>
      </div>
    </q-toolbar>
  </q-header>
</template>
