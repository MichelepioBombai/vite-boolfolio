<script>
import AppHeader from "./components/AppHeader.vue";

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

  components: { AppHeader },
};
</script>

<template>
  <AppHeader :title="title" />
  <main class="container">
    <router-view></router-view>
  </main>
</template>

<style lang="scss"></style>
