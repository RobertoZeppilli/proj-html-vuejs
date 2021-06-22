<template>
  <header>
    <div class="header__fixed">
      <div class="container">
        <div class="header__logo">
          <img class="logo" src="../assets/img/Logo.jpg" alt="Logo" />
        </div>
        <nav class="header__nav">
          <Links
            v-for="(navLink, index) in navLinks"
            :key="index"
            :singleLink="navLink"
          />
        </nav>
      </div>
    </div>
    <Jumbotron />
  </header>
</template>

<script>
import Links from "./Links";
import Jumbotron from "./Jumbotron";

export default {
  name: "Header",
  props: {
    navLinks: Array,
  },
  components: {
    Links,
    Jumbotron,
  },
};
</script>

<style lang="scss">
@import "../scss/general";

header {

  .header__fixed {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 4;
    width: 100%;
    background-color: #fff;
  }
  .container {
    width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
  }
}
.header__logo {
  & > .logo {
    height: 130px;
    position: absolute;
    z-index: 3;
  }
}
.header__nav {
  display: flex;
  align-items: center;
  line-height: 80px;

  li {
    margin-left: 35px;

    a {
      text-decoration: none;
      color: #3c4955;
      font-weight: bold;
    }
  }
}
</style>