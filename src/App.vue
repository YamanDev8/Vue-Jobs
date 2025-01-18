<script>
export default {
  data() {
    return {
      name: "Yaman",
      status: false,
      tasks: ["task1", "task2", "task3"],
    };
  },
};
</script>

<template>
  <h1>Hello world</h1>
  <h3>{{ name }}</h3>
  <p v-if="status">user is active</p>
  <p v-else>user is inactive</p>
  <ul>
    <li v-for="task in tasks" :key="task"></li>
  </ul>
</template>
