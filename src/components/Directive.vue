<script setup>
const favColor = "orange";
</script>
<template>
  <div class="w-[500px] mx-auto my-10 border p-10">
    <h3 class="text-center font-bold text-2xl mb-5">Favorit Color</h3>
    <input
      class="bg-transparent border p-3 w-full text-white"
      v-model="favColor"
      type="text"
      placeholder="type your favorit color name"
    />
    <p
      :class="{ 'text-blue-700': favColor == 'blue' }"
      v-if="favColor == 'blue'"
    >
      My Favorit color is Blue
    </p>
    <p
      :class="{ 'text-red-700': favColor == 'red' }"
      v-else-if="favColor == 'red'"
    >
      My Favorit color is red
    </p>
    <p
      :class="{ 'text-yellow-700': favColor == 'yellow' }"
      v-else-if="favColor == 'yellow'"
    >
      My Favorit color is yellow
    </p>
    <p
      :class="{ 'text-green-700': favColor == 'green' }"
      v-else-if="favColor == 'green'"
    >
      My Favorit color is green
    </p>
    <p
      :class="{ 'text-purple-700': favColor == 'purple' }"
      v-else-if="favColor == 'purple'"
    >
      My Favorit color is purple
    </p>
    <p
      :class="{ 'text-pink-700': favColor == 'pink' }"
      v-else-if="favColor == 'pink'"
    >
      My Favorit color is pink
    </p>
    <p
      :class="{ 'text-orange-700': favColor == 'orange' }"
      v-else-if="favColor == 'orange'"
    >
      My Favorit color is orange
    </p>
    <p class="text-error" v-else>I don't know</p>
  </div>
</template>
