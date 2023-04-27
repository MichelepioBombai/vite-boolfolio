<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import ProjectList from "./components/ProjectList.vue";

export default {
  data() {
    return {
      title: "Vue Boolpress",
      projects: {
        list: [],
        pagination: [],
      },
    };
  },

  methods: {
    fetchProjects() {
      axios.get("http://127.0.0.1:8000/api/projects").then((response) => {
        this.projects.list = response.data.data;
      });
    },
  },

  created() {
    this.fetchProjects();
  },

  components: { AppHeader, ProjectList },
};
</script>

<template>
  <AppHeader :title="title" />
  <ProjectList
    :projects="projects.list"
    :pagination="projects.pagination"
    title="Most Recent "
    class="my-4"
  />
</template>

<style lang="scss"></style>
