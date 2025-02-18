<template>
    <div class="p-4 borders rounded shadow-lg mt-4">
      <h2 class="text-lg font-bold">Local Storage Counter</h2>
      <button @click="count--" class="px-4 py-2 bg-blue-500 text-white rounded">-</button>
      <button @click="count = 0" class="px-4 py-2 bg-blue-500 text-white rounded">Reset</button>
      <button @click="count++" class="px-4 py-2 bg-red-500 text-white rounded">+</button>
      <p>Count: {{ count }}</p>
    </div>
  </template>
  
  <script setup lang="ts">
  import { useLocalStorage } from '@vueuse/core';
  
  const count = useLocalStorage('vueuse-counter', 0);
  </script>
  
