<template>
  <div class="footer__top__register">
    <div class="footer__top__register__container">
      <div class="footer__top__subscribe">
        <input placeholder="Subscribe to our newsletter" type="text" />
        <input type="submit" value="Register" />
      </div>
      <div class="footer__top__cta">
        <p>
          <span>Insights is Picwik</span> thought leadership publication for
          sharing knowledge on management, technology and innovation
        </p>
        <a href="#">Take me There <i class="fas fa-chevron-right"></i></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Register",
};
</script>

<style lang="scss">
.footer__top__register {
  height: 150px;
  padding: 30px 0;
  background-color: #192735;
  box-shadow: 5px 5px 5px 5px #172532;
  margin-bottom: 80px;
}
.footer__top__register__container {
  display: flex;
  height: 100%;
  padding: 10px 30px;
  border-left: 7px solid #23374b;
}
.footer__top__subscribe {
  height: 100%;
  width: 50%;

  input[type="text"] {
    height: 100%;
    width: 60%;
    padding: 0 20px;
    border-radius: 0;
    outline: none;
    border: none;
  }
  input[type="submit"] {
    height: 100%;
    width: 20%;
    border-radius: 0;
    outline: none;
    border: none;
    color: #fff;
    background-color: #d74d52;
    cursor: pointer;
  }
}
.footer__top__cta {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  width: 50%;
  p {
    color: #8fa1b5;
    line-height: 20px;
  }
  span {
    color: #d74d52;
    font-weight: bold;
    position: relative;

    &::after {
      content: '';
      position: absolute;
      bottom: -3px;
      left: 0;
      height: 1px;
      width: 100%;
      background-color: #fff;
    }
  }
  a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
  }
  i {
    font-size: 12px;
  }
}
</style>