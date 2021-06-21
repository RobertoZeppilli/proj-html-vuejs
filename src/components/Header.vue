<template>
  <header>
    <div class="container">
      <div class="header__container">
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
  .header__container {
    display: flex;
    justify-content: space-between;
    height: 80px;
  }
}
.header__logo {
  & > .logo {
    height: 130px;
  }
}
.header__nav {
  display: flex;
  align-items: center;
  line-height: 80px;

  li {
    margin: 0 10px;

    a {
      text-decoration: none;
      color: #3c4955;
      font-weight: bold;
    }
  }
}
</style>