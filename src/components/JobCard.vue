<template>
  <div
    class="flex items-center justify-center"
    style="
      background-color: rgba(255, 255, 255, 0.4);
      width: 56px;
      height: 56px;
      border-radius: 8px;
    "
  >
    <component :is="job.icon" />
  </div>
  <div style="font-size: 24px">{{ job.name }}</div>
</template>

<script setup>
defineProps(["job"]);
</script>
