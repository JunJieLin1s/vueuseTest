<!-- MouseTracker.vue -->
<template>
    <div class="p-4 border rounded shadow-lg">
        <h2 class="text-lg font-bold">Mouse Tracker</h2>
        <p>X: {{ x }}, Y: {{ y }}</p>
    </div>
</template>

<script setup lang="ts">
    import { useMouse } from '@vueuse/core';

    const { x, y }: { x: Ref<number>; y: Ref<number> } = useMouse();
</script>
  
