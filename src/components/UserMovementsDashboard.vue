<script setup lang="ts">
import UserStats from './UserStats.vue';
</script>

<template>
  <section class="layout container">
    <!-- Total, Mountly, Weekly report -->
    <UserStats/>
    <!-- Data graph -->
    <!-- Register new movent-->
  </section>
</template>

<style scoped>
  .layout {
    display: grid;
    width: 100%;
    grid-template-rows: min-content auto min-content;
  }
</style>