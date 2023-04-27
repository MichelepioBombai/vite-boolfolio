<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";

export default {
  data() {
    return {
      projects: [],
    };
  },

  methods: {
    fetchProjects() {
      axios.get("http://127.0.0.1:8000/api/projects").then((response) => {
        this.projects = response.data;
      });
    },
  },

  created() {
    this.fetchProjects();
  },

  components: { AppHeader },
};
</script>

<template>
  <AppHeader />
  <h1>hello world</h1>
  <ul>
    <li v-for="project in projects">{{ project.title }}</li>
  </ul>
</template>

<style lang="scss"></style>
