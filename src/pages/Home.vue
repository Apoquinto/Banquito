<script setup lang="ts">
import SplashScreen from '../components/SplashScreen.vue';
import { defineAsyncComponent } from 'vue'

const UserResume = defineAsyncComponent(() =>
  import('../components/UserResume.vue')
)
</script>

<template>
  <SplashScreen/>
<!--   <main class="grid place-items-center w-screen h-screen">
    <span>Oh no, estoy vivo <i class='bx bx-line-chart text-xl'></i></span>
  </main> -->
</template>