<template>
  <footer>
    <FooterTop
      :supportLinks="supportLinks"
      :exploreLinks="exploreLinks"
      :visitLinks="visitLinks"
      :contacts="contacts"
    />
    <FooterBottom :supportLinks="supportLinks" />
  </footer>
</template>

<script>
import FooterTop from "./FooterTop";
import FooterBottom from "./FooterBottom";

export default {
  name: "Footer",
  components: {
    FooterTop,
    FooterBottom,
  },
  props: {
    supportLinks: Array,
    exploreLinks: Array,
    visitLinks: Array,
    contacts: Array,
  },
};
</script>

<style lang="scss">
@import '../scss/variables';
@import '../scss/mixins';

footer {
  background-color: $darkBackground;
  position: relative;
  &::after {
    @include square ($type: 'default');
  }

  .footer__top {
    padding: 70px 0;
    .footer__nav {
      @include flex($type: 'justify between');
      color: $white;

      li {
        a {
          color: $grey;
          text-decoration: none;
          transition: color .5s ease-in-out;
          &:hover {
            color: $red;
          }
        }
      }
    }
  }
}
</style>