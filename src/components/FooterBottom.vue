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
.footer__bottom {
  height: 50px;
  background-color: #15222e;
  .container {
    height: 100%;
  }
  .footer__bottom__container {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #8fa1b5;
  }
  .footer__bottom__nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    li {
      margin-left: 10px;
      a {
        text-decoration: none;
        color: #8fa1b5;
        font-size: .8rem;
      }
    }
  }
  i {
      display: none;
  }
}
</style>