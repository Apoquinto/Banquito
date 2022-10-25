<script setup lang="ts">
import StatReport from './StatReport.vue';
</script>

<template>
  <section class="flex flex-col md:flex-row justify-around gap-5 w-full">
    <StatReport :amount=400 :label="'Total windraw'"></StatReport>
    <StatReport :amount=500 :label="'Monthly in'"></StatReport>
    <StatReport :amount=100 :label="'Monthly out'"></StatReport>
  </section>
</template>