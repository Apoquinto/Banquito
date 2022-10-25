<script setup lang="ts">
import StatReport from './StatReport.vue';
</script>

<template>
  <section class="flex flex-col md:flex-row justify-around gap-5 w-full">
    <StatReport :amount=1000 :label="'Total amount'"></StatReport>
    <StatReport :amount=500 :label="'Monthly amount'"></StatReport>
    <StatReport :amount=100 :label="'Weekly amount'"></StatReport>
  </section>
</template>