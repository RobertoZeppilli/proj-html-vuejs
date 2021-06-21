<template>
  <ul>
    <li>
      <a :href="singleLink.url"><i v-if="singleLink.icon == true" :class="`${singleLink.family} ${singleLink.type}`"></i> {{ singleLink.name }}</a>
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

<style lang="scss">
    ul {
        list-style: none;
    }
</style>