<script setup lang="ts">
import SplashScreen from '../components/SplashScreen.vue';
import { defineAsyncComponent } from 'vue'

const UserResume = defineAsyncComponent(() => import('../components/UserResume.vue'))
</script>

<template>
  <Suspense>
    <UserResume/>
    <template #fallback>
      <SplashScreen/>
    </template>
  </Suspense>
</template>