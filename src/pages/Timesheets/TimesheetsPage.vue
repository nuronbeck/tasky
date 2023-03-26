<script setup lang="ts">
import RoundedBox from 'components/Boxes/RoundedBox/RoundedBox.vue';
</script>

<template>
  <q-page class="q-pa-lg">
    <h3 class="text-bold">Timesheets</h3>

    <div class="row q-col-gutter-lg">
      <div class="col-12 col-md-4">
        <RoundedBox>
          <h5>Weekly Activity</h5>
        </RoundedBox>
      </div>

      <div class="col-12 col-md-4">
        <RoundedBox>
          <h5>Worked This Week</h5>
        </RoundedBox>
      </div>

      <div class="col-12 col-md-4">
        <RoundedBox>
          <h5>Project Worked</h5>
        </RoundedBox>
      </div>
    </div>
  </q-page>
</template>
