<template>
  <section id="academics">
    <div class="academics__title">
      <h2>Recent Courses</h2>
      <p>
        Whether you're considering a foundation course or an undergraduate
        degree master's or a PhD, academics is a place where students thrive.
      </p>
    </div>
    <div class="academics">
      <div class="academic" v-for="(academic, index) in academics" :key="index">
        <div class="academic__img">
          <img :src="academic.courseImg" alt="" />
        </div>
        <div class="academic__info">
          <p class="academic__price">{{ academic.price }}</p>
          <h3>{{ academic.course }}</h3>
          <p class="academic__description">{{ academic.description }}</p>
          <p class="academic__distributor">Course by: {{ academic.distributor }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Academics",
  props: {
    academics: Array,
  },
};
</script>

<style lang="scss">
@import "../scss/variables";
@import "../scss/mixins";

#academics {
  padding-top: 100px;
  .academics__title {
    text-align: center;
    width: 70%;
    margin: 0 auto 70px;
    p {
      @include paragraphSize ($type: 'default');
    }
  }
  .academics {
    @include flex($type: "justify between");
    .academic {
      width: calc(100% / 3 - 1rem);
      box-shadow: $mainBoxesShadow;
      .academic__img {
        height: 250px;
        img {
          @include imagePosition($type: "cover top");
        }
      }
      .academic__info {
        padding: 30px 20px;
        h3 {
          font-size: 1.5rem;
          margin: 15px 0 20px 0;
        }
        .academic__price {
          position: relative;
          font-weight: bold;
          z-index: 1;

          &::before {
            @include pinkHighlight($type: "default");
          }
        }
        .academic__description {
          margin-bottom: 40px;
          @include paragraphSize ($type: 'default');
        }
        .academic__distributor {
          color: $red;
        }
      }
    }
  }
}
</style>