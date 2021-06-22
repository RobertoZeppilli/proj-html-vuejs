<template>
  <section id="pictures">
    <div class="pictures">
      <div class="picture" v-for="picture,index in pictures" :key="index">
          <img :src="picture.img" alt="">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Pictures",
  props: {
    pictures: Array,
  },
};
</script>

<style lang="scss">
#pictures {
    margin-top: 100px;
}
.pictures {
  display: flex;
  border-bottom: 2px solid #fff;
}
.picture {
  height: 300px;
  width: calc(100% / 4);
  img {
      width: 100%;
      height: 100%;
      object-fit: cover;
  }
}
</style>