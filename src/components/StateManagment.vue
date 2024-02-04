<script setup>
import { ref } from "vue";
const imgLink = "https://th.bing.com/th/id/OIG.MxQxUggA0RKmKdTjwAqw";
const alt = "Fox Image";
const desc =
  " A fox is a small carnivorous mammal with a pointed snout and dense bushy tail. They are found throughout the world, and are known for their feline-like agility and cunning. Foxes are omnivores, and eat a varied diet that includes fruits, vegetables, and small animals. They are  ";

const count = ref(0);
const showFox = ref(false)
const showInfo = ref(false)
</script>
<template>
  <div>
    <Transition type="animation" name="bounce">

      <img v-if="showFox" class="w-[500px] mx-auto" :src="imgLink" :alt="alt" />
    </Transition>
    <Transition type="animation" name="bounce">

      <p v-if="showInfo" class="w-[500px] mx-auto font-sans mt-5">{{ desc }}</p>

    </Transition>
    <div class="justify-center flex gap-10 mt-5">
      <button @click="showFox = !showFox" class="btn btn-primary">Toggole Fox</button>
      <button @click="showInfo = !showInfo" class="btn btn-primary">Toggole Info</button>
    </div>
  </div>
  <div class="mt-5 rounded-2xl w-[500px] mx-auto border text-center p-10">
    <button @click="count++" class="btn btn-outline btn-accent">Add 1</button>
    <button
      v-if="count > 0"
      @click="count--"
      class="btn btn-outline btn-warning ml-5"
    >
      Remove 1
    </button>
    <p class="text-4xl font-mono py-3">{{ count }}</p>
  </div>
</template>
<style scoped>
.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}</style>
