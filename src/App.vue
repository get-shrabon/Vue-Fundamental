<script setup>
import Looping from './components/Looping.vue';
// import CountryFilter from './components/CountryFilter.vue';
// import StateManagment from './components/StateManagment.vue';
// import Directive from './components/Directive.vue';
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="flex justify-center gap-10">
    <a href="/" >
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="/" >
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <Looping/>
<!--  <CountryFilter/>
  <HelloWorld/>
  <Directive/>
  <StateManagment/> -->
</template> 

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
