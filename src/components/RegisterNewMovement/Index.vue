<script setup lang="ts">import { ref } from 'vue';
import Modal from "../Modal.vue"
import NewMovementForm from './NewMovementForm.vue';

const isOpen = ref(false);
  
const toggleModal = () => isOpen.value = !isOpen.value;
</script>

<template>
  <button
    @click="toggleModal" 
    class="w-fit bg-slate-500 hover:bg-slate-600 active:bg-slate-700 focus:outline-none focus:ring focus:ring-indigo-300 border-x rounded-lg text-white flex justify-center items-center px-2 py-3">
    Register new movement 
  </button>
  <teleport to="#app">
    <Modal 
      v-show="isOpen"
      :title="'New movement'"
      @close="toggleModal">
      <NewMovementForm/>
    </Modal>
  </teleport>
</template>