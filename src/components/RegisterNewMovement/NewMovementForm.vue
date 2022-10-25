<script setup lang="ts">
import { reactive, ref } from 'vue';
import { Movement } from '../../types/Movement';

const newMovement: Movement = reactive({
  title: "",
  description: "",
  amount: null,
  createdAt: new Date(Date.now())
});
const movementType = ref("");

const submit = () => {
  console.log(newMovement);
}
</script>

<template>
  <form @submit.prevent="submit" class="flex flex-col gap-5">
    <div class="w-full h-fit flex flex-col">
      <label>Title</label>
      <input class="px-2 py-1 border rounded" type="text" v-model="newMovement.title" placeholder="A movement title...">
    </div>
    <div class="w-full h-fit flex flex-col">
      <label>Amount</label>
      <input class="px-2 py-1 border rounded" type="text" v-model="newMovement.amount" placeholder="0">
    </div>
    <div class="w-full h-fit flex flex-col">
      <label>Description</label>
      <textarea class="px-2 py-1 border rounded" type="text" v-model="newMovement.description" placeholder="Some sort of description..."/>
    </div>
    <div class="w-full h-fit flex flex-col">
      <label>Type</label>
      <label><input v-model="movementType" class="mr-1" type="radio" value="entry">Entry</label>
      <label><input v-model="movementType" class="mr-1" type="radio" value="spent">Spent</label>
    </div>
    <div>
      <button class="w-full bg-indigo-500 hover:bg-indigo-600 active:bg-indigo-700 focus:outline-none focus:ring focus:ring-indigo-300 border-x rounded-xl text-white flex justify-center items-center py-2">
        Save movement
      </button>
    </div>
  </form>
</template>