<script>
export default {
  props: {
    project: Object,
  },

  computed: {
    abstract() {
      return this.project.text.slice(0, 120) + "...";
    },
  },
};
</script>

<template>
  <div>
    <div class="card">
      <div class="card-header">
        <h2>{{ project.title }}</h2>
      </div>
      <div class="card-body">
        {{ abstract }}
      </div>
      <div class="card-footer">Created at {{ project.created_at }}</div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
