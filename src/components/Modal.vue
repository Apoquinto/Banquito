<script setup lang="ts">
import { defineEmits, toRefs } from "vue";

const emit = defineEmits(["close"]);
const props = defineProps<{
    title: string
}>();
const { title } = toRefs(props); 

const close = () => emit("close");
</script>

<template>
    <div class="overflow-y-auto overflow-x-hidden fixed top-0 right-0 md:inset-0 z-50 w-full h-full bg-slate-900/25">
        <div class="h-full w-full grid place-content-center">
            <div class="modal bg-white border rounded px-3 py-2">
                <div class="head flex justify-between items-center">
                    <h1 class="font-medium">{{ title }}</h1>
                    <button @click="close">
                        <span class="bx bx-x text-2xl"></span>
                    </button>
                </div>
                <div class="body">
                    <slot></slot>
                </div>
            </div>
            
        </div>
    </div>
</template>

<style scoped>
    .modal {
        width: 75vh;
        height: fit-content;
    }
</style>