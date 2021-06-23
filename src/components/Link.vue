<template>
  <a href="#">{{ linktext }}<i class="fas fa-chevron-right"></i></a>
</template>

<script>
export default {
  name: "Link",
  props: {
    linktext: String,
  },
};
</script>

<style lang="scss">
@import "../scss/variables";

a {
  text-decoration: none;
  color: $darkText;
  transition: color 0.5s ease-in-out;
  &:hover {
    color: $red;
  }

  i {
    margin-left: 5px;
    font-size: 12px;
  }
}
</style>