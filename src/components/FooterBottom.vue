<template>
  <div class="footer__bottom">
    <div class="container">
      <div class="footer__bottom__container">
        <div class="footer__bottom__copyright">
          <h6>&copy; Copyright 2020 tophive. All Rights Reserved.</h6>
        </div>
        <div class="footer__bottom__nav">
          <Links
            v-for="(supportLink, index) in supportLinks"
            :key="index"
            :singleLink="supportLink"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Links from "./Links";
export default {
  name: "FooterBottom",
  components: {
    Links,
  },
  props: {
    supportLinks: Array,
  },
};
</script>

<style lang="scss">
@import "../scss/variables";
@import "../scss/mixins";

.footer__bottom {
  height: 50px;
  background-color: $footerBottomBg;
  .container {
    height: 100%;
    .footer__bottom__container {
      height: 100%;
      @include flex($type: "between");
      color: $grey;
      .footer__bottom__nav {
        @include flex($type: "between");
        li {
          margin-left: 10px;
          a {
            text-decoration: none;
            color: $grey;
            font-size: 0.8rem;
            transition: color 0.5s ease-in-out;
            &:hover {
              color: $red;
            }
          }
          i {
            display: none;
          }
        }
      }
    }
  }
}
</style>