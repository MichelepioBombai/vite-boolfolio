<script>
export default {
  props: {
    project: Object,
  },
};
</script>

<template>
  <ul>
    <li>
      {{ project.title }}
    </li>
  </ul>
</template>

<style lang="scss" scoped></style>
