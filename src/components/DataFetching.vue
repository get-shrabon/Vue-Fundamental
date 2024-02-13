<script setup>
import { reactive, ref } from "vue";

const users = reactive([]);
const searchData = ref("");

const getData = () => {
  fetch("https://jsonplaceholder.typicode.com/users")
    .then((res) => res.json())
    .then((data) => {
      data.forEach((user) => {
        users.push(user);
      });
    });
};

getData();
const getUsers = () => {
  if (searchData.value) {
    return users.filter((user) => {
      if (user.name.includes(searchData.value)) {
        return user;
      }
    });
  } else {
    return users;
  }
};
</script>

<template>
  <input
    class="p-3 border-0 outline-0 w-64"
    type="text "
    v-model="searchData"
  />
  <button @click="searchData = ''" class="btn btn-outline btn-info ml-4">
    Clear
  </button>
  <ul class="space-y-4">
    <li v-for="(user, index) in getUsers()" :key="index" class="flex flex-col">
      <span>Name: {{ user.name }}</span>
      <span>Email: {{ user.email }}</span>
    </li>
  </ul>
</template>
