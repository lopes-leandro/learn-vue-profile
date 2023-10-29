<script setup lang="ts">
import AppHeader from "./components/AppHeader.vue";
import AppProfileForm from "./components/AppProfileForm.vue";
import AppProfileDisplay from "./components/AppProfileDisplay.vue";
import { reactive } from "vue";

const formData = reactive({name: ""});
function update(e) {
  formData.name = e.name;
}
</script>

<template>
  <AppHeader />
  <div class="flex flex-col md:flex-row">
    <AppProfileForm @submit="update($event)"/>
    <AppProfileDisplay :form-data="formData"/>
  </div>
</template>

<style scoped></style>
