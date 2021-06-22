<template>
  <section id="services">
    <h2>
      Since 2000, we've been partnering with education leaders to
      <span>increase equity and achievement</span> for all students
    </h2>
    <div class="services">
      <div
        class="service__info"
        v-for="(service, index) in services"
        :key="index"
      >
        <div class="service">
          <img :src="service.img" :alt="service.service" />
          <h3>{{ service.service }}</h3>
          <p>{{ service.description }}</p>
        </div>
        <div class="numbers">
          <p
            :style="{
              backgroundImage: `url(${service.bgGreen}), url(${service.bgRed}), url(${service.bgOrange})`,
            }"
          >
            <span
              :class="{
                orange: service.backgroundColor == 'orange',
                red: service.backgroundColor == 'red',
                green: service.backgroundColor == 'green',
              }"
              >{{ service.numbers }}</span
            >
          </p>
          <p class="type">{{ service.type }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Services",
  props: {
    services: Array,
  },
};
</script>

<style lang="scss">
h2 {
  text-align: center;
  line-height: 50px;
  width: 90%;
  margin: 30px auto;
  font-size: 2.3rem;
  span {
    color: #d74d52;
  }
}
.services {
  display: flex;
  justify-content: space-between;
  .service__info {
    display: flex;
    flex-direction: column;
    width: calc(100% / 3 - 1rem);
    .service {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      text-align: center;
      padding: 50px 30px 60px 30px;
      margin: 50px 0;
      box-shadow: 2px 2px 2px 2px #ebebeb;
      img {
        width: 70px;
      }
      h3 {
        margin: 20px 0;
        font-size: 1.5rem;
      }
      p {
        font-size: 1.3rem;
        line-height: 30px;
      }
    }

    .numbers {
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      p {
        font-size: 3rem;
        display: inline-block;
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        font-weight: bold;
      }
      .red,
      .orange {
        &::after {
          content: "+";
          font-size: 3rem;
          margin-left: 10px;
          font-weight: bold;
        }
      }
      .orange {
        color: orange;
      }
      .red {
        color: red;
      }
      .green {
        color: green;

        &::after {
          content: "%";
          font-size: 3rem;
          margin-left: 10px;
          font-weight: bold;
        }
      }
      .type {
        font-size: 1.4rem;
        margin-left: 10px;
      }
    }
  }
}
</style>