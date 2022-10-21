<script setup lang="ts">
  const userData = await new Promise((resolve) => {
    setTimeout(() => {
      console.log("Data loaded");
      resolve(true);
    }, 2000);
  });
</script>

<template>
  <main class="grid place-items-center w-screen h-screen">
    UserHome
  </main>
</template>