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
footer {
  background-color: #192735;
  .footer__top {
    padding: 70px 0;
    .footer__nav {
      display: flex;
      justify-content: space-between;
      color: #fff;

      li {
        // margin-top: 20px;
        a {
          color: #8fa1b5;
          text-decoration: none;
        }
      }
    }
  }
}
</style>