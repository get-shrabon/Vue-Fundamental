<script setup>
import { ref } from "vue";
import Plus from "../assets/Plus.png";
import Minus from "../assets/minus.png";

const accordionItems = ref([
  {
    title: "Introduction to Programming",
    description:
      "Learn the fundamentals of programming, including variables, control structures, and basic algorithms.",
    isOpen: true,
  },
  {
    title: "Web Development Basics",
    description:
      "Explore the essentials of web development, covering HTML, CSS, and JavaScript to build interactive websites.",
    isOpen: false,
  },
  {
    title: "Data Science Fundamentals",
    description:
      "Dive into data science concepts such as data analysis, statistics, and machine learning basics.",
    isOpen: false,
  },
  {
    title: "Mobile App Development",
    description:
      "Discover the world of mobile app development using frameworks like React Native or Flutter.",
    isOpen: false,
  },
  {
    title: "Database Management",
    description:
      "Understand database concepts, design, and management using popular systems like MySQL or MongoDB.",
    isOpen: false,
  },
  {
    title: "Cybersecurity Essentials",
    description:
      "Learn the basics of cybersecurity, including encryption, network security, and threat detection.",
    isOpen: false,
  },
]);


</script>

<template>
  <div class="w-[500px] mx-auto">
    <!-- Header -->
    <div
      v-for="(item, index) in accordionItems"
      :key="index"
      class="w-full p-3 rounded-xl bg-slate-800 mb-4"
    >
      <div
        @click="item.isOpen = !item.isOpen"
        class="flex items-center justify-between cursor-pointer select-none"
      >
        <h3>{{ item.title }}</h3>
        <img class="w-6" :src="item.isOpen ? Minus : Plus" alt="" />
      </div>
      <!-- Content -->

      <div v-if="item.isOpen" class="pt-4">
        {{ item.description }}
      </div>
    </div>
  </div>
</template>
