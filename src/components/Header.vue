<script setup lang="ts">
  const reload = () => location.reload();
</script>

<template>
  <header class="w-full flex justify-between px-5 py-2 border-b">
     <img src="../assets/icon.svg" alt="logo" @click=reload>
     <h2 class=" text-indigo-500">Banquito</h2>
  </header>
</template>