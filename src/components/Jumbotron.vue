<template>
  <div class="jumbotron">
    <div class="jumbotron__text">
      <h1>professional development for coaches and leaders</h1>
    </div>
    <div class="jumbotron__cta">
      <a href="#">learn more</a>
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
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-image: url(../assets/img/02_Landing-Page.jpg);
  background-repeat: no-repeat;
  height: 1100px;
  background-size: cover 70%;
  background-position: center;

  .jumbotron__text {
    width: 60%;
    h1 {
      text-align: center;
      font-size: 4rem;
      text-transform: capitalize;
      font-weight: 400;
      font-family: "Times New Roman", Times, serif;
    }
  }
  .jumbotron__cta {
    margin-top: 30px;
    border: 1px solid #191919;
    padding: 15px 40px;
    cursor: pointer;

    a {
      text-decoration: none;
      color: #191919;
      text-transform: capitalize;
    }
  }
}
</style>