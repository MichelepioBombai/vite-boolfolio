<script>
import axios from "axios";
import ProjectCard from "../components/ProjectCard.vue";

export default {
  name: "ProjectDetailPage",
  data() {
    return {
      project: null,
    };
  },

  created() {
    console.log(this.$route.params.id);

    axios
      .get(`http://127.0.0.1:8000/api/projects/${this.$route.params.id}`)
      .then((response) => {
        this.project = response.data;
      });
  },
  components: { ProjectCard },
};
</script>

<template>
  <h1 class="my-4">Dettaglio Progetto</h1>
  <ProjectCard v-if="project" :project="project" :isDetail="true" />
</template>

<style></style>
