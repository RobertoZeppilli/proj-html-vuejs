<template>
  <div class="jumbotron">
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
.jumbotron {
  position: relative;
  background-image: url(../assets/img/02_Landing-Page.jpg);
  background-repeat: no-repeat;
  height: 1000px;
  // background-color: #ebebeb;
  background-size: cover;
  background-position: left bottom;

  .jumbotron__text {
    width: 60%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    h1 {
      text-align: center;
      font-size: 4rem;
      text-transform: capitalize;
      font-weight: 400;
      margin-bottom: 40px;
      font-family: "Times New Roman", Times, serif;
    }
    span {
      display: inline-block;
      text-decoration: none;
      color: #191919;
      text-transform: capitalize;
      border: 1px solid #191919;
      padding: 15px 40px;
      cursor: pointer;
    }
  }
}
</style>