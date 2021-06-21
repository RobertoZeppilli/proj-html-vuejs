<template>
  <div class="footer__top">
    <nav class="footer__nav">
      <div>
        <h4 class="footer__nav__title">Contact Us</h4>
        <Contacts
          v-for="(contact, index) in contacts"
          :key="index"
          :singleContact="contact"
        />
      </div>
      <div>
        <h4 class="footer__nav__title">Support Us</h4>
        <Links
          v-for="(supportLink, index) in supportLinks"
          :key="index"
          :singleLink="supportLink"
        />
      </div>
      <div>
        <h4 class="footer__nav__title">Explore</h4>
        <Links
          v-for="(exploreLink, index) in exploreLinks"
          :key="index"
          :singleLink="exploreLink"
        />
      </div>
      <div>
        <h4 class="footer__nav__title">Visit</h4>
        <Links
          v-for="(visitLink, index) in visitLinks"
          :key="index"
          :singleLink="visitLink"
        />
      </div>
    </nav>
  </div>
</template>

<script>
import Links from "./Links";
import Contacts from "./Contacts";

export default {
  name: "FooterTop",
  components: {
    Links,
    Contacts,
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
    .footer__nav__title {
        margin-bottom: 20px;
        font-size: 1.4rem;
    }
</style>