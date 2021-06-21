<template>
  <header>
    <nav>
      <Links
        v-for="(navLink, index) in navLinks"
        :key="index"
        :singleLink="navLink"
      />
    </nav>
  </header>
</template>

<script>
import Links from "../components/Links";
export default {
  name: "Header",
  props: {
    navLinks: Array,
  },
  components: {
    Links,
  },
};
</script>

<style lang="scss">
header {
  height: auto;
  background-color: red;
}
</style>