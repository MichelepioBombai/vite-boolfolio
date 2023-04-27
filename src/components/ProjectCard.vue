<script>
export default {
  props: {
    project: Object,
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
        {{ project.text }}
      </div>
      <div class="card-footer">Created at {{ project.created_at }}</div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
