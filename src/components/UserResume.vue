<script setup lang="ts">
import UserHistoryAccordion from './UserHistoryAccordion.vue';

const userData = await new Promise((resolve) => {
  setTimeout(() => {
    console.log("Data loaded");
    resolve(true);
  }, 2000);
});
</script>

<template>
  <main class="grid place-items-center w-full h-full">
    UserHome
  </main>
  <UserHistoryAccordion/>
</template>