<template>
  <section id="news">
    <div class="news__title">
      <h2>Latest From Our Blogs</h2>
      <p>
        Whether you're considering a foundation course or an undergraduate
        degree master's or a PhD, academics is a place where students thrive.
      </p>
    </div>
    <div class="news">
      <div class="notice" v-for="(blog, index) in blogs" :key="index">
        <div class="notice__img">
          <img :src="blog.img" alt="blog image" />
        </div>
        <div class="notice__info">
          <div class="notice__icons">
            <p>
              <i :class="`${blog.family} ${blog.type2}`"></i>{{ blog.profile }}
            </p>
            <p>
              <i :class="`${blog.family} ${blog.type1}`"></i>{{ blog.class }}
            </p>
          </div>
          <h3>{{ blog.text }}</h3>
          <Link linktext="Read More" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Link from "./Link";
export default {
  name: "News",
  props: {
    blogs: Array,
  },
  components: {
    Link,
  },
};
</script>

<style lang="scss">
@import '../scss/variables';
@import '../scss/mixins';

#news {
  margin-top: 100px;
  padding-top: 100px;
  .news__title {
    text-align: center;
    width: 70%;
    margin: 0 auto 40px;

    h2 {
      margin-bottom: $h2Margin;
      font-size: $h2Size;
    }

    p {
      @include paragraphSize ($type: 'default');
    }
  }
  .news {
    @include flex($type: 'justify between');
    .notice {
      width: calc(100% / 3 - 1rem);
      box-shadow: $mainBoxesShadow;
      .notice__img {
        height: 250px;
        img {
          @include imagePosition ($type: 'cover top');
        }
      }
      .notice__info {
        padding: 30px 20px;
        h3 {
          position: relative;
          font-size: 1.5rem;
          margin: 15px 0 70px 0;
          &::after {
            @include redLine ($type: 'default');
          }
        }
        .notice__icons {
          display: flex;
          p:nth-child(1) {
            margin-right: 30px;
          }
          i {
            margin-right: 5px;
          }
        }
      }
    }
  }
}
</style>