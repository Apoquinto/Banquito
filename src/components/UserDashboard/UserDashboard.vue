<script setup lang="ts">
import UserStats from './UserStats.vue';
import RegisterNewMovement from "../RegisterNewMovement/Index.vue";
</script>

<template>
  <section class="layout container">
    <!-- Total, Mountly, Weekly report -->
    <UserStats/>
    <!-- Data graph -->
    <section class="h-full">
    </section>
    <!-- Register new movent-->
    <section class="w-full grid place-content-center">
      <RegisterNewMovement/>
    </section>
  </section>
</template>

<style scoped>
  .layout {
    display: grid;
    width: 100%;
    grid-template-rows: min-content auto min-content;
  }
</style>