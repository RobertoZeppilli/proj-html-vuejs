<template>
  <section id="courses">
    <div class="courses__title">
      <h2>Recent Courses</h2>
      <p>
        Whether you're considering a foundation course or an undergraduate
        degree master's or a PhD, academics is a place where students thrive.
      </p>
    </div>
    <div class="courses">
      <div class="course" v-for="(course, index) in courses" :key="index">
        <div class="course__img">
          <img :src="course.courseImg" alt="" />
        </div>
        <div class="course__info">
          <p class="price">{{ course.price }}</p>
          <h3>{{ course.course }}</h3>
          <p class="description">{{ course.description }}</p>
          <p class="distributor">Course by: {{ course.distributor }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: "Courses",
  props: {
    courses: Array,
  }
};
</script>

<style lang="scss">
#courses {
  margin-top: 100px;
  .courses__title {
    text-align: center;
    width: 70%;
    margin: 0 auto 70px;

    p {
      font-size: 1.3rem;
    }
  }
  .courses {
    display: flex;
    justify-content: space-between;
    .course {
      width: calc(100% / 3 - 1rem);
      box-shadow: 2px 2px 2px 2px #ebebeb;
      .course__img {
        height: 250px;
        img {
          height: 100%;
          width: 100%;
          object-fit: cover;
          object-position: top;
        }
      }
      .course__info {
        padding: 30px 20px;
        h3 {
          font-size: 1.5rem;
          margin: 15px 0 20px 0;
        }
        .price {
          position: relative;
          font-weight: bold;
          z-index: 1;

          &::before {
            content: "";
            position: absolute;
            z-index: -1;
            bottom: 0;
            background-color: rgba(255, 192, 203, 0.5);
            height: 10px;
            width: 11%;
          }
        }
        .description {
          margin-bottom: 40px;
          font-size: 1.3rem;
          line-height: 30px;
        }
        .distributor {
          color: #d74d52;
        }
      }
    }
  }
}
</style>