<script lang="ts" setup>
import styles from './RoundedBox.module.scss';
</script>

<template>
  <div :class="styles.box">
    <slot />
  </div>
</template>
