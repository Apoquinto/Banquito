<script setup lang="ts">
import { computed, ref, toRefs } from "vue";
const props = defineProps<{
    id: number,
    title: string,
    description: string,
    createdAt: Date,
    amount: number
}>();
const emit = defineEmits(["remove"])
const { id, title, description, createdAt, amount } = toRefs(props);

const remove = () => {
    emit("remove", id.value)
};

const amountState = computed(() => ({
    'text-green-600': amount.value >= 0,
    'text-red-600': amount.value < 0
}))

const formatAmount = computed(() => {
  const formatter = new Intl.NumberFormat('en-US', {
    style: 'currency',
    currency: 'MXN',
  });
  return formatter.format(amount.value);
})
</script>

<template>
    <div class="w-screen grid grid-row-2 px-5 py-2 border-b">
        <div class="title flex justify-between items-center">
            <h1 class="font-bold">{{ title }}</h1>
            <button @click="remove">
                <span class="bx bx-trash text-red-400 text-xl pr-2"></span>
            </button>            
        </div>
        <div class="info">
            <span :class="amountState">{{ formatAmount }}</span>
            <p>{{ description }}</p>
        </div>
    </div>
</template>