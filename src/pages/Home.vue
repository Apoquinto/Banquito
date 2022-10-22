<script setup lang="ts">
import Header from '../components/Header.vue';
import { defineAsyncComponent } from 'vue'
import MenuLayout from "../layouts/MenuLayout.vue"

const UserResume = defineAsyncComponent(() => import('../components/UserResume.vue'))
</script>

<template>
  <MenuLayout>
    <template #header>
      <Header/>
    </template>
    <template #default>
      <UserResume/>
    </template>
  </MenuLayout>
</template>