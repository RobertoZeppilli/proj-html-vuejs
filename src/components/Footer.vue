<template>
  <footer>
    <div class="container">
      <FooterTop
        :supportLinks="supportLinks"
        :exploreLinks="exploreLinks"
        :visitLinks="visitLinks"
        :contacts="contacts"
      />
    </div>
  </footer>
</template>

<script>
import FooterTop from "./FooterTop";


export default {
  name: "Footer",
  components: {
    FooterTop,
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
    padding: 50px 0;
    .footer__nav {
      display: flex;
      justify-content: space-between;
      margin-top: 30px;
      color: #fff;

      li {
        margin-top: 10px;
        a {
          color: #8fa1b5;
          text-decoration: none;
        }
      }
    }
  }
}
</style>