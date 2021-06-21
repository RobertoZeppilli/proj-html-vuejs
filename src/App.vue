<template>
  <div id="app">
    <Header :navLinks="Links" />
    <Main />
    <Footer :supportLinks="Supports" :exploreLinks="Explores" :visitLinks="Visits"/>
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
    Footer
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
          name: 'Privacy',
          url: '#privacy'
        },
        {
          name: 'Terms',
          url: '#terms'
        },
        {
          name: 'Cookie Policy',
          url: '#cookie-policy'
        },
        {
          name: 'Sitemap',
          url: '#sitemap'
        }
      ],
      Explores: [
        {
          name: 'Accomodation',
          url: '#accomodation'
        },
        {
          name: 'Arts Academics',
          url: '#arts-academics'
        },
        {
          name: 'Central Services',
          url: '#central-services'
        },
        {
          name: 'Conferences and Events',
          url: '#conferences'
        },
        {
          name: 'Food and Drink',
          url: '#food-and-drink'
        },
      ],
      Visits: [
        {
          name: 'Admission',
          url: '#admission'
        },
        {
          name: 'Contact Us',
          url: '#contact-us'
        },
        {
          name: 'FAQs',
          url: '#faqs'
        },
        {
          name: 'Request Information',
          url: '#request-information'
        },
        {
          name: 'Privacy Notice',
          url: '#privacy-notice'
        }
      ],
      Contacts: [
        {
          icon: '<i class="fas fa-map-marker-alt"></i>',
          text: '900, Wood Street, MI New York 48607'
        },
        {
          icon: '<i class="fas fa-phone-square-alt"></i>',
          text: '+ 56 345 678 000-09'
        },
        {
          icon: '<i class="fas fa-envelope"></i>',
          text: 'info@example.com'
        }
      ]
    };
  },
};
</script>

<style lang="scss">
@import './scss/general';

</style>
