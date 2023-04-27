<script>
export default {
  name: "AppHeader",
  props: {
    title: String,
  },
};
</script>

<template>
  <nav class="navbar bg-body-tertiary">
    <div class="container">
      <a class="navbar-brand" href="#">{{ title }}</a>
    </div>
  </nav>
</template>

<style lang="scss"></style>
