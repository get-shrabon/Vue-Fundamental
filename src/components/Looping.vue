<script setup>
const tasks = [
  { id: 1, task: "Complete project proposal", status: "In Progress" },
  { id: 2, task: "Review design mockups", status: "Pending" },
  { id: 3, task: "Implement new feature", status: "To Do" },
  { id: 4, task: "Test application", status: "Done" },
  { id: 5, task: "Prepare documentation", status: "Done" },
  { id: 6, task: "Meeting with the team", status: "Pending" },
  { id: 7, task: "Bug fixing", status: "To Do" },
  { id: 8, task: "User interface enhancements", status: "In Progress" },
  { id: 9, task: "Code refactoring", status: "Pending" },
  { id: 10, task: "Write unit tests", status: "To Do" },
  { id: 11, task: "Deploy to production", status: "In Progress" },
  { id: 12, task: "Client meeting", status: "Pending" },
  { id: 13, task: "Optimize database queries", status: "To Do" },
  { id: 14, task: "Prepare release notes", status: "Done" },
  { id: 15, task: "Create user training materials", status: "In Progress" },
];
</script>
<template>
  <h2 class="text-center py-10 text-3xl font-bold font-mono text-primary">
    Hello World from Lopping With Vue.js
  </h2>
  <div class="gap-5 text-center">
    <div>
      <h3 class="text-info text-xl mb-5">In Progresive Work</h3>
      <ul class="grid grid-cols-4 w-full gap-5">
        <li
          class="flex items-center flex-col bg-slate-800 w-full hover:bg-slate-700 p-3 mx-auto"
          v-for="task in tasks"
          :key="task.id"
        >
          <span class="font-bold">{{ task.task }}</span>
          <span class="text-slate-300 " :class="'Done' == task.status && 'line-through'">{{ task.status }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>
