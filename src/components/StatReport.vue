<script setup lang="ts">
import { computed, toRefs } from 'vue';

const props = defineProps({
  amount: {
    type: Number,
    default: 0,
  },
  label: {
    type: String,
    required: true,
  }
});

const { amount, label } = toRefs(props)

// Remember replace this with a composable.
const formatAmount = computed(() => {
  const formatter = new Intl.NumberFormat('en-US', {
    style: 'currency',
    currency: 'MXN',
  });
  return formatter.format(amount.value);
})
</script>

<template>
  <div class="bg-slate-700 text-white border border-slate-800 w-full h-full flex px-10 py-2 rounded-xl">
    <div class="w-full h-full flex flex-col">
      <h3 class="text-2xl font-bold">{{ formatAmount }}</h3>
      <span>{{ label }}</span>
    </div>
  </div>
</template>