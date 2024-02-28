<script setup>
import { ref } from "vue";
const select = ref("");
const checkbox = ref([]);
</script>
<template>
  <p class="text-primary text-xl mb-3">Selected: {{ select }}</p>
  <select v-model="select" class="select select-primary w-[500px] mb-5">
    <option v-for="index in 6" :key="index" :value="`Option ${index} `">
      Option {{ index }}
    </option>
  </select>
  <p class="text-primary text-xl mb-3">Your Fav Colors is: {{ checkbox }}</p>
  <div class="flex gap-3">
    <input
      v-model="checkbox"
      class="checkbox"
      value="Orange"
      type="checkbox"
      name=""
      id="check1"
    />
    <label for="check1"> Blue </label>
  </div>
  <div class="flex gap-3 my-3">
    <input
      v-model="checkbox"
      class="checkbox"
      value="Blue"
      type="checkbox"
      name=""
      id="check2"
    />
    <label for="check2"> Yellow </label>
  </div>
  <div class="flex gap-3">
    <input
      v-model="checkbox"
      class="checkbox"
      value="Yellow"
      type="checkbox"
      name=""
      id="check3"
    />
    <label for="check3"> Orange </label>
  </div>
  <div class="flex gap-3 mt-3">
    <input
      v-model="checkbox"
      class="checkbox"
      value="Pink"
      type="checkbox"
      name=""
      id="check4"
    />
    <label for="check4"> Pink </label>
  </div>
</template>
<style scoped></style>
