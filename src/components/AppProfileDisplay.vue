<template>
  <section class="md:w-1/3 h-64 bg-blue-200 flex p-12">
    <h3 class="font-bold font-lg">{{ formData.name }}</h3>
  </section>
</template>
<script setup lang="ts">
const props = defineProps({formData: Object});
</script>
<style scoped></style>
