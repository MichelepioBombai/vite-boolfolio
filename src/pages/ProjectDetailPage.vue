<script>
import ProjectCard from "../components/ProjectCard.vue";

export default {
  name: "ProjectDetailPage",
  data() {
    return {};
  },

  created() {
    console.log(this.$route.params.id);
  },
  components: { ProjectCard },
};
</script>

<template>
  <h1 class="my-4">Dettaglio Progetto</h1>
</template>

<style></style>
