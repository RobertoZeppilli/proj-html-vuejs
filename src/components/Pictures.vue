<template>
  <section id="pictures">
    <div class="pictures">
      <div class="picture" v-for="(picture, index) in pictures" :key="index">
        <img :src="picture.img" alt="" />
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
@import "../scss/mixins";
@import "../scss/variables";

#pictures {
  margin-top: 100px;
  .pictures {
    display: flex;
    border-bottom: 2px solid $white;
    .picture {
      height: 300px;
      width: calc(100% / 4);
      img {
        @include imagePosition($type: "cover");
      }
    }
  }
}
</style>