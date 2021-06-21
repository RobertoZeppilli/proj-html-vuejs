<template>
  <ul>
    <li>
      <a :href="singleLink.url">{{ singleLink.name }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "Links",
  props: {
    singleLink: Object,
  },
};
</script>

<style lang="scss" scoped>
</style>