<template>
  <main class="w-screen h-screen layout">
    <slot name="header"></slot>
    <slot></slot>
    <slot name="history"></slot>
  </main>
</template>


<style scoped>
  .layout {
    display: grid;
    grid-template-rows: min-content auto min-content;
  }
</style>