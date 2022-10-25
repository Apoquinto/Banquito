<script setup lang="ts">
import { defineAsyncComponent } from 'vue'
import Header from '../../components/Header.vue';
import MenuLayout from "../../layouts/MenuLayout.vue"

const UserResume = defineAsyncComponent(() => import('../../components/UserDashboard/Index.vue'))
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