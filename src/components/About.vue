<template>
  <section id="about">
    <div class="about__title">
      <h2>
        Since 2000, we've been partnering with education leaders to
        <span>increase equity and achievement</span> for all students
      </h2>
    </div>
    <div class="abouts">
      <div class="about__info" v-for="(about, index) in abouts" :key="index">
        <div class="about">
          <img :src="about.img" :alt="about.about" />
          <h3>{{ about.about }}</h3>
          <p>{{ about.description }}</p>
        </div>
        <div class="about__numbers">
          <p
            :style="{
              backgroundImage: `url(${about.bgGreen}), url(${about.bgRed}), url(${about.bgOrange})`,
            }"
          >
            <span
              :class="{
                orange: about.backgroundColor == 'orange',
                red: about.backgroundColor == 'red',
                green: about.backgroundColor == 'green',
              }"
              >{{ about.numbers }}</span
            >
          </p>
          <p class="type">{{ about.type }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
  props: {
    abouts: Array,
  },
};
</script>

<style lang="scss">
@import "../scss/mixins";
@import "../scss/variables";

#about {
  padding-top: 100px;
  .about__title {
    h2 {
      text-align: center;
      line-height: 50px;
      width: 90%;
      margin: 30px auto;
      font-size: 2.3rem;
      span {
        color: $red;
      }
    }
  }
  .abouts {
    @include flex($type: "justify between");
    .about__info {
      @include flex($type: "column");
      width: calc(100% / 3 - 1rem);
      .about {
        @include flex($type: "column between align-center");
        text-align: center;
        padding: 50px 30px 60px 30px;
        margin: 50px 0;
        box-shadow: $mainBoxesShadow;
        img {
          width: 70px;
        }
        h3 {
          margin: 20px 0;
          font-size: 1.5rem;
        }
        p {
          @include paragraphSize($type: "default");
        }
      }

      .about__numbers {
        @include flex($type: "center");
        text-align: center;
        p {
          display: inline-block;
          @include setBackground($type: "contain");
          font-size: 3rem;
          font-weight: bold;
        }
        .red,
        .orange {
          &::after {
            content: "+";
            @include operatorSize($type: "default");
          }
        }
        .orange {
          color: $orangeNumber;
        }
        .red {
          color: $redNumber;
        }
        .green {
          color: $greenNumber;

          &::after {
            content: "%";
            @include operatorSize($type: "default");
          }
        }
        .type {
          font-size: 1.4rem;
          margin-left: 10px;
        }
      }
    }
  }
}
</style>