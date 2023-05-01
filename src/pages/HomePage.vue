<script>
import axios from "axios";
import ProjectList from "../components/ProjectList.vue";
export default {
  data() {
    return {
      projects: {
        list: [],
        pagination: [],
      },
    };
  },

  components: { ProjectList },

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
};
</script>
<template>
  <ProjectList
    :projects="projects.list"
    :pagination="projects.pagination"
    title="Most Recent "
    class="my-4"
  />
</template>

<style lang="scss" scoped></style>
