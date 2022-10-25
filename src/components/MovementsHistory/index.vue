<script setup lang="ts">
import MovementCard from './Movement.vue';
import { Ref, ref } from 'vue';

const isOpen = ref(false);
const message = ref("Show details")
const toggleAccordion = () => {
isOpen.value = !isOpen.value
message.value = !isOpen.value? "Show details": "Close details";
};
const movements = ref([
{
    id: 1,
    title: "Test",
    description: "Test",
    createdAt: new Date(Date.now()),
    amount: 1000,
},
{
    id: 2,
    title: "Test",
    description: "Test",
    createdAt: new Date(Date.now()),
    amount: -1000,
}
]);

const removeMovement = (id: number) => {
    console.log("remove", id);
}
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
      class="layout grid place-content-start" 
      v-show="isOpen"
    >
        <div class="w-full">
            <MovementCard
                v-for="{id, title, description, createdAt, amount} in movements"
                :key="id"
                :id="id"
                :title="title"
                :description="description"
                :created-at="createdAt"
                :amount="amount"
                @remove="removeMovement"
            />
        </div>
    </section>
  </section>
</template>

<style scoped>
  .layout {
    height: 75vh;
    width: 100%;
  }
</style>