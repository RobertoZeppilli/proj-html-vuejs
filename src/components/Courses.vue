<template>
  <section id="courses">
    <div class="testimonial">
      <p class="testimonial__text">
        "Academics was committed to my success from the moment I attended an
        Open House. With the support of caring
        <span class="red">advisors, professors, and staff </span>I was able to
        thrive in courses, gain recognition through scolarships, and finish
        <span class="bold"
          >with confidence in my
          <span class="red">@academics</span> abilities.</span
        >"
      </p>
    </div>
    <div class="events">
      <div class="event__one">
        <img
          class="video"
          src="../assets/img/video-bg-3.jpg"
          alt="Video Frame"
        />
        <img class="play" src="../assets/img/play-button.png" alt="" />
      </div>
      <div class="event__two">
        <div class="flag">
          <h3>Upcoming Events</h3>
        </div>
        <div class="event__info">
          <p>
            Princeton offers admission information sessions and student-led
            tours to campus visitors
          </p>
          <Link linktext="Learn More" />
        </div>
        <div class="event__info">
          <p>
            Admission information sessions and student-led tours to campus
            visitors
          </p>
          <Link linktext="Learn More" />
        </div>
        <div class="event__cta">
          <i class="far fa-map"></i>
          <Link linktext="Event Locations" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Link from "./Link";
export default {
  name: "Courses",
  props: {
    events: Array,
  },
  components: {
    Link,
  },
};
</script>

<style lang="scss" scoped>
@import "../scss/variables";
@import "../scss/mixins";

#courses {
  padding-top: 100px;
  .testimonial {
    width: 90%;
    margin: 0 auto;
    padding: 20px 0;
    @include setBackground($type: "testimonial");
    .testimonial__text {
      font-size: 1.9rem;
      text-align: center;
      line-height: 50px;

      .red {
        color: $red;
        font-weight: bold;
        position: relative;
        &::before {
          @include redLine($type: "testimonial");
        }
      }
      .bold {
        font-weight: bold;
      }
    }
  }
  .events {
    position: relative;
    @include flex($type: "justify between");
    margin-top: 50px;
    .event__one,
    .event__two {
      width: calc(100% / 2);
      box-shadow: $mainBoxesShadow;
    }
    .event__one {
      position: relative;
      .video {
        height: 100%;
        object-fit: cover;
      }
      &::after {
        @include play($type: "default");
      }
      .play {
        @include absoluteCenter($type: "default");
        height: 40px;
        z-index: 20;
      }
    }
    .event__two {
      position: absolute;
      top: 15%;
      left: 35%;
      width: 55%;
      padding: 0 50px 60px 50px;
      background-color: $white;
      .flag {
        @include flex($type: "center");
        height: 100px;
        width: 50%;
        margin: 0 auto;
        text-align: center;
        background-color: $red;
        color: $white;
        h3 {
          font-size: 1.4rem;
        }
      }
      .event__info {
        padding: 0 30px;
        p {
          margin: 40px 0 20px 0;
          font-weight: bold;
          @include paragraphSize($type: "default");
        }
        a {
          font-weight: bold;
        }
      }
      .event__cta {
        margin-top: 80px;
        text-align: center;
        a {
          font-weight: bold;
        }
        i {
          margin-right: 5px;
        }
      }
    }
  }
}
</style>