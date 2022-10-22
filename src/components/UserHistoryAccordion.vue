<script setup lang="ts">
import { ref } from 'vue';
  const isOpen = ref(false);
  const message = ref("Show details")
  const toggleAccordion = () => {
    isOpen.value = !isOpen.value
    message.value = !isOpen.value? "Show details": "Close details";
  };
</script>

<template>
  <section class="w-full h-fit border-t">
    <button 
      class="w-full bg-indigo-500 hover:bg-indigo-600 active:bg-indigo-700 focus:outline-none focus:ring focus:ring-indigo-300 border-x rounded-t-xl text-white flex justify-center items-center py-3"
      @click="toggleAccordion"
    >
      <span class="bx bx-math text-2xl pr-2"></span>{{ message }}
    </button>
    <section 
      class="layout text-slate-400 grid place-content-center" 
      v-show="isOpen"
    >
      <span class="w-fit">*Insert Content*</span>
    </section>
  </section>
</template>

<style scoped>
  .layout {
    height: 75vh;
  }
</style>