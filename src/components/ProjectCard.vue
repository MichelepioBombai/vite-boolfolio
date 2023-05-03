<script>
export default {
  props: {
    project: Object,
    isDetail: Boolean,
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
        {{ isDetail ? project.text : abstract }}
      </div>
      <div class="card-footer d-flex justify-content-between">
        Created at {{ project.created_at }}
        <router-link
          v-if="!isDetail"
          :to="{
            name: 'project-detail',
            params: {
              id: project.id,
            },
          }"
          class="btn btn-primary btn-sm"
        >
          Vedi
        </router-link>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
