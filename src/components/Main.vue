<template>
  <main>
    <div class="container">
      <About :abouts="Abouts" />
      <Academics :academics="Academics" />
      <Courses />
      <News :blogs="News"/>
    </div>
    <Pictures :pictures="Pictures"/>
  </main>
</template>

<script>
import About from "./About";
import Academics from "./Academics";
import Courses from "./Courses";
import News from "./News";
import Pictures from "./Pictures";

export default {
  name: "Main",
  components: {
    About,
    Academics,
    Courses,
    News,
    Pictures
  },
  data() {
    return {
      Abouts: [
        {
          img: require("../assets/svg/svg-0.svg"),
          service: "Online Coaching",
          description:
            "Lorem ipsum is simply dummy text of the print ing and typesetting has been the industries",
          numbers: "6500",
          type: "Students",
          backgroundColor: "orange",
          bgOrange: require("../assets/img/counter-shape-1-1-1.png"),
        },
        {
          img: require("../assets/svg/svg-1.svg"),
          service: "Consultation",
          description:
            "Lorem ipsum is simply dummy text of the print ing and typesetting has been the industries",
          numbers: "200",
          type: "Online Courses",
          backgroundColor: "red",
          bgRed: require("../assets/img/counter-shape-2-1-1.png"),
        },
        {
          img: require("../assets/svg/svg-2.svg"),
          service: "Life Programs",
          description:
            "Lorem ipsum is simply dummy text of the print ing and typesetting has been the industries",
          numbers: "100",
          type: "Happy Clients",
          backgroundColor: "green",
          bgGreen: require("../assets/img/counter-shape-3-1-1.png"),
        },
      ],
      Academics: [
        {
          courseImg: require("../assets/img/bruce-mars-FWVMhUa_wbY-unsplash.jpg"),
          price: "Free",
          course: "UI animation using Sketch 3, Principle App and Flinto",
          description:
            "This online photography course will teach you how to take amazing images and even sell...",
          distributor: "University",
        },
        {
          courseImg: require("../assets/img/course-1-2.jpg"),
          price: "Free",
          course: "The Ultimate Drawing Course - Beginner to Advanced",
          description:
            "This online photography course will teach you how to take amazing images and even sell...",
          distributor: "University",
        },
        {
          courseImg: require("../assets/img/william-thomas-ny6tO4ItOEY-unsplash.jpg"),
          price: "Free",
          course: "Your Complete Guide to Photography",
          description:
            "This online photography course will teach you how to take amazing images and even sell...",
          distributor: "University",
        },
      ],
      News: [
        {
          img: require("../assets/img/news-3-2.jpg"),
          text: "Peer pressure changes how teens tackle inequality",
          profile: 'Admin',
          class: 'University',
          family: 'far',
          type1: 'fa-folder',
          type2: 'fa-user'
        },
        {
          img: require("../assets/img/success-1.jpg"),
          text: "Lewisham Live Mixtape celebrates  borough's",
          profile: 'Admin',
          class: 'Education',
          family: 'far', 
          type1: 'fa-folder',
          type2: 'fa-user'
        },
        {
          img: require("../assets/img/success-2.jpg"),
          text: "Turner Prize winner's work to open Gold on Film festival",
          profile: 'Admin',
          class: 'Education',
          family: 'far',
          type1: 'fa-folder',
          type2: 'fa-user'
        },
      ],
      Pictures: [
        {
          img: require("../assets/img/academy-1.jpg")
        },
        {
          img: require("../assets/img/academy-2.jpg")
        },
        {
          img: require("../assets/img/academy-3.jpg")
        },
        {
          img: require("../assets/img/academy-4.jpg")
        }
      ]
    };
  },
};
</script>

<style lang="scss" scoped>

</style>