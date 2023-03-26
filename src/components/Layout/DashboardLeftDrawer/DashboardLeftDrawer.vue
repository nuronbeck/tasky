<script setup lang="ts">
import AppLogo from 'components/Layout/AppLogo/AppLogo.vue';
// import styles from './DashboardLeftDrawer.module.scss';
</script>

<template>
  <div>
    <div class="flex flex-center q-pa-lg">
      <AppLogo />
    </div>

    <div class="q-pa-lg">
      <q-tabs vertical inline-label class="text-dark">
        <q-route-tab
          class="text-capitalize"
          name="movies"
          icon="movie"
          label="Dashboard"
          to="/"
          exact
          active-class="bg-secondary text-white"
        />

        <q-route-tab
          class="text-capitalize"
          name="mails"
          icon="mail"
          label="Timesheets"
          to="/timesheets"
          exact
          active-class="bg-secondary text-white"
        />
      </q-tabs>
    </div>
  </div>
</template>
