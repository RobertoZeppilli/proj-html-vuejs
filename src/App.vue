<template>
  <div id="app">
    <Header :navLinks="Links" />
    <Main />
    <Footer
      :supportLinks="Supports"
      :exploreLinks="Explores"
      :visitLinks="Visits"
      :contacts="Contacts"
    />
  </div>
</template>

<script>
import Header from "./components/Header";
import Main from "./components/Main";
import Footer from "./components/Footer";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      Links: [
        {
          name: "Home",
          url: "#home",
        },
        {
          name: "About",
          url: "#about",
        },
        {
          name: "Academics",
          url: "#academics",
        },
        {
          name: "Courses",
          url: "#courses",
        },
        {
          name: "News",
          url: "#news",
        },
      ],
      Supports: [
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Privacy",
          url: "#privacy",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Terms",
          url: "#terms",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Cookie Policy",
          url: "#cookie-policy",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Sitemap",
          url: "#sitemap",
        },
      ],
      Explores: [
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Accomodation",
          url: "#accomodation",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Arts Academics",
          url: "#arts-academics",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Central Services",
          url: "#central-services",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Conferences and Events",
          url: "#conferences",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Food and Drink",
          url: "#food-and-drink",
        },
      ],
      Visits: [
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Admission",
          url: "#admission",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Contact Us",
          url: "#contact-us",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "FAQs",
          url: "#faqs",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Request Information",
          url: "#request-information",
        },
        {
          icon: true,
          family: "fas",
          type: "fa-chevron-right",
          name: "Privacy Notice",
          url: "#privacy-notice",
        },
      ],
      Contacts: [
        {
          family: "fas",
          type: "fa-map-marker-alt",
          text: "900, Wood Street, MI New York 48607",
        },
        {
          family: "fas",
          type: "fa-phone-square-alt",
          text: "+ 56 345 678 000-09",
        },
        {
          family: "fas",
          type: "fa-envelope",
          text: "info@example.com",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./scss/general";
</style>
