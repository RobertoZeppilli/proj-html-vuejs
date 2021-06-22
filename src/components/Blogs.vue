<template>
  <section id="blogs">
    <div class="blogs__title">
      <h2>Latest From Our Blog</h2>
      <p>
        Whether you're considering a foundation course or an undergraduate
        degree master's or a PhD, academics is a place where students thrive.
      </p>
    </div>
    <div class="blogs">
      <div class="blog" v-for="(blog, index) in blogs" :key="index">
        <div class="blog__img">
          <img :src="blog.img" alt="" />
        </div>
        <div class="blog__info">
          <div class="blog__icons">
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
  name: "Blogs",
  props: {
    blogs: Array,
  },
  components: {
    Link,
  },
};
</script>

<style lang="scss">
#blogs {
    // margin-top: 100px;
  padding-top: 120px;
  .blogs__title {
    text-align: center;
    width: 70%;
    margin: 0 auto 70px;

    p {
      font-size: 1.3rem;
    }
  }
  .blogs {
    display: flex;
    justify-content: space-between;
    .blog {
      width: calc(100% / 3 - 1rem);
      box-shadow: 2px 2px 2px 2px #ebebeb;
      .blog__img {
        height: 250px;
        img {
          height: 100%;
          width: 100%;
          object-fit: cover;
          object-position: top;
        }
      }
      .blog__info {
        padding: 30px 20px;
        h3 {
          position: relative;
          font-size: 1.5rem;
          margin: 15px 0 70px 0;
          &::after {
            content: "";
            position: absolute;
            bottom: -25px;
            left: 0;
            height: 2px;
            width: 20%;
            background-color: #d74d52;
          }
        }
        .blog__icons {
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