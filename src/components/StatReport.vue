<script setup lang="ts">
import { toRefs } from 'vue';

const props = defineProps({
  amount: Number,
  label: String
})

const { amount, label } = toRefs(props)
</script>

<template>
  <div class="bg-slate-700 text-white border border-slate-800 w-full h-full flex px-10 py-2 rounded-xl">
    <div class="w-full h-full flex flex-col">
      <h3 class="text-2xl font-bold">${{ amount }}</h3>
      <span>{{ label }}</span>
    </div>
  </div>
</template>