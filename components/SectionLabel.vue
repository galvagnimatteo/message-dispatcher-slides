<script setup lang="ts">
defineProps<{ label: string }>()
</script>

<template>
  <div class="section-label">
    <span class="teal-dot" />
    <span class="section-label-text">{{ label }}</span>
  </div>
</template>
