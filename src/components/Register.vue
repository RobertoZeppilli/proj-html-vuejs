<template>
  <div class="footer__top__register">
    <div class="footer__top__register__container">
      <div class="footer__top__subscribe">
        <input placeholder="Subscribe to our newsletter" type="text" />
        <input type="submit" value="Register" />
      </div>
      <div class="footer__top__cta">
        <p>
          <span>Insights is Picwik</span> thought leadership publication for
          sharing knowledge on management, technology and innovation
        </p>
        <a href="#">Take me There <i class="fas fa-chevron-right"></i></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Register",
};
</script>

<style lang="scss">
@import "../scss/mixins";
@import "../scss/variables";

.footer__top__register {
  height: 150px;
  padding: 30px 0;
  background-color: $darkBackground;
  box-shadow: $footerBoxShadow;
  margin-bottom: 80px;
  .footer__top__register__container {
    display: flex;
    height: 100%;
    padding: 10px 30px;
    border-left: $registerBorder;
    .footer__top__subscribe {
      height: 100%;
      width: 50%;

      input[type="text"] {
        height: 100%;
        width: 60%;
        padding: 0 20px;
        @include inputReset($type: "default");
      }
      input[type="submit"] {
        height: 100%;
        width: 20%;
        @include inputReset($type: "default");
        color: $white;
        background-color: $red;
        cursor: pointer;
        transition: all 0.5s ease-in-out;
        &:hover {
          color: $red;
          background-color: $white;
          border-left: 1px solid $red;
        }
      }
    }
    .footer__top__cta {
      @include flex($type: "column between");
      height: 100%;
      width: 50%;
      p {
        color: $grey;
        line-height: 20px;
      }
      span {
        color: $red;
        font-weight: bold;
        position: relative;

        &::after {
          @include underline($type: "default");
        }
      }
      a {
        text-decoration: none;
        color: $white;
        font-weight: bold;
        transition: color 0.5s ease-in-out;
        &:hover {
          color: $red;
        }
      }
      i {
        font-size: 12px;
      }
    }
  }
}
</style>