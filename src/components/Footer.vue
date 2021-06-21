<template>
  <footer>
    <nav>
      <div>
        <h4>Support</h4>
        <Links
          v-for="(supportLink, index) in supportLinks"
          :key="index"
          :singleLink="supportLink"
        />
      </div>
      <div>
        <h4>Explore</h4>
        <Links
          v-for="(exploreLink, index) in exploreLinks"
          :key="index"
          :singleLink="exploreLink"
        />
      </div>
      <div>
        <h4>Visit</h4>
        <Links
          v-for="(visitLink, index) in visitLinks"
          :key="index"
          :singleLink="visitLink"
        />
      </div>
    </nav>
  </footer>
</template>

<script>
import Links from "./Links";

export default {
  name: "Footer",
  components: {
    Links
  },
  props: {
    supportLinks: Array,
    exploreLinks: Array,
    visitLinks: Array
  },
};
</script>

<style lang="scss" scoped>
footer {
  background-color: yellow;
  height: auto;
}
</style>