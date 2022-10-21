<script setup lang="ts">
import SplashScreen from './components/SplashScreen.vue';
import Home from './pages/Home.vue';
</script>

<template>
  <Suspense>
    <Home/>
    <template #fallback>
      <SplashScreen/>
    </template>
  </Suspense>
</template>