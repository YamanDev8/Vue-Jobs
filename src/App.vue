<script>
export default {
  data() {
    return {
      name: "Yaman",
      status: false,
      tasks: ["task1", "task2", "task3"],
      link: "https://google.com",
    };
  },
  methods: {
    toggleStatus() {
      if (this.status) {
        this.status = false;
      } else if (!this.status) {
        this.status = true;
      }
    },
  },
};
</script>

<template>
  <h1>Hello world</h1>
  <h3>{{ name }}</h3>
  <p v-if="status">user is active</p>
  <p v-else>user is inactive</p>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  <a :href="link">Go to google</a>
  <br />
  <button v-on:click="toggleStatus">Toggle status</button>
</template>
