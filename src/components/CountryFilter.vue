<script setup>
import { ref } from "vue";

const activeCountry = ref("Bangladash");
const handleCountry = () => {
  const inputCountryName = prompt("Please Type Country Name");
  activeCountry.value = capitalize(inputCountryName);
};
const capitalize = (str) => {
  return str.charAt(0).toUpperCase() + str.slice(1);
};
</script>
<template>
  <div class="w-[fit-content] py-20 mx-auto">
    <h2 class="pb-5 text-info">
      Bangladash, India, Bhutan, Nepal, Pakistan Countries Information
    </h2>
    <ul>
      <li
        class="w-[300px] p-5 bg-slate-800"
        v-show="activeCountry == 'Bangladash'"
      >
        <h2 class="font-semibold text-xl">Country: Bangladesh</h2>
        <p><span class="font-bold text-lg">Capital:</span> Dhaka</p>
        <p><span class="font-bold text-lg">Population:</span> 166 million</p>
        <p><span class="font-bold text-lg">Area:</span> 147,570 km²</p>
      </li>
      <li class="w-[300px] p-5 bg-slate-800" v-show="activeCountry == 'India'">
        <h2 class="font-semibold text-xl">Country: India</h2>
        <p><span class="font-bold text-lg">Capital:</span> New Delhi</p>
        <p><span class="font-bold text-lg">Population:</span> 1.366 billion</p>
        <p><span class="font-bold text-lg">Area:</span> 3.29 million km²</p>
      </li>
      <li class="w-[300px] p-5 bg-slate-800" v-show="activeCountry == 'Bhutan'">
        <h2 class="font-semibold text-xl">Country: Bhutan</h2>
        <p><span class="font-bold text-lg">Capital:</span> Thimphu</p>
        <p><span class="font-bold text-lg">Population:</span> 771,608</p>
        <p><span class="font-bold text-lg">Area:</span> 38,394 km²</p>
      </li>
      <li class="w-[300px] p-5 bg-slate-800" v-show="activeCountry == 'Nepal'">
        <h2 class="font-semibold text-xl">Country: Nepal</h2>
        <p><span class="font-bold text-lg">Capital:</span> Kathmandu</p>
        <p><span class="font-bold text-lg">Population:</span> 29 million</p>
        <p><span class="font-bold text-lg">Area:</span> 147,516 km²</p>
      </li>
      <li
        class="w-[300px] p-5 bg-slate-800"
        v-show="activeCountry == 'Pakistan'"
      >
        <h2 class="font-semibold text-xl">Country: Pakistan</h2>
        <p><span class="font-bold text-lg">Capital:</span> Islamabad</p>
        <p><span class="font-bold text-lg">Population:</span> 225 million</p>
        <p><span class="font-bold text-lg">Area:</span> 881,913 km²</p>
      </li>
    </ul>
    <button @click="handleCountry" class="btn btn-info mt-5">
      Set Country Name
    </button>
  </div>
</template>
