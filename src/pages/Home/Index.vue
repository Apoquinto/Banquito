<script setup lang="ts">
import SplashScreen from '../SplashScreen/Index.vue';
import Home from '../Home/Home.vue';
</script>

<template>
  <Suspense>
    <Home/>
    <template #fallback>
      <SplashScreen/>
    </template>
  </Suspense>
</template>