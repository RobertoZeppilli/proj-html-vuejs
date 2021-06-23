<template>
  <div id="home" class="jumbotron">
    <div class="jumbotron__text">
      <h1>professional development for coaches and leaders</h1>
      <span>learn more</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Jumbotron",
};
</script>

<style lang="scss">
@import "../scss/mixins";

.jumbotron {
  position: relative;
  height: 1000px;
  @include setBackground($type: "jumbotron");

  .jumbotron__text {
    width: 60%;
    @include absoluteCenter($type: "default");
    text-align: center;
    h1 {
      @include jumbotronTextStyle($type: "default");
    }
    span {
      @include jumbotronButton($type: "default");
      &:hover {
        color: $red;
        border-color: $red;
      }
    }
  }
}
</style>