<template>
  <section class="md:w-2/3 flex flex-col p-12 items-center bg-red-200">
    <div class="flex flex-col">
      <label for="name" class="flex text-gray-800 mb-2">Nome</label>
      <input
        type="text"
        name="name"
        id="name"
        class="border-2 border-solid border-blue-200 rounded px-2 py-1"
        v-model="name"
      />
    </div>
    <div class="flex flex-row mt-12">
      <button type="submit" @click="formSubmit()">Enviar</button>
    </div>
  </section>
</template>
<script setup lang="ts">
import { ref } from "vue";
const emit = defineEmits(["submit"]);
const name = ref("");

const formSubmit = () => {
  emit("submit", {
    name: name,
  });
}
</script>
<style scoped></style>
