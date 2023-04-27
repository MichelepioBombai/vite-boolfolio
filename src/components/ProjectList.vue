<script>
import ProjectCard from "./ProjectCard.vue";

export default {
  props: {
    projects: Array,
    title: String,
    pagination: Array,
  },

  components: { ProjectCard },
};
</script>

<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <div class="row g-4">
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :project="project"
        class="col-md-4 d-flex"
      />
    </div>
    <nav aria-label="Projects pagination">
      <ul class="pagination my-4">
        <li class="page-item">
          <a class="page-link" href="#">1</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<style lang="scss" scoped></style>
