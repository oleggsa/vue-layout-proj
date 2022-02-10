<template>
  <section class="get-started__wrapper">
    <div class="get-started__content-wrapper">
      <div class="get-started__content">
        <div class="get-started__content-title">
          MARKETING TOOLKIT <br>FOR INSTAGRAM
        </div>
        <div class="get-started__content-desqr">
          Become Instagram-famous and skyrocket sales by using pro tools. These must-have solutions
          will help you attract fans, engage with сustomers, сurate content, and grow revenue.
        </div>
        <div class="get-started__content-btns">
          <MyButton>GET STARTED</MyButton>
          <div class="get-started__second-button">
            <a href="#"><p>CHECK YOUR GROWTH</p></a>
            <GradientRectangle></GradientRectangle>
          </div>
        </div>
      </div>
      <div class="get-started__images">
        <img class="get-started__images-icons" src="../images/header-robot-icons.png" alt="icons">
        <img class="get-started__images-robot" src="../images/header-robot.png" alt="robot">
        <img class="get-started__images-bottom" src="../images/header-robot-under.png" alt="bottom">
      </div>
    </div>
  </section>
</template>

<script>


export default {
  name: "GetStarted",

}
</script>

<style lang="scss" scoped>

  .get-started {
    &__wrapper {
      height: 550px;
      background-image: url('../images/header-background.png');
      background-repeat: no-repeat;
      margin-top: 80px;
    }
    &__content-wrapper {
      margin: 0 140px;
    }
    &__content {
      width: 580px;
      display: inline-block;
      &-title {
        padding-top: 60px;
        font-size: 36px;
        font-weight: 600;
        color: #FFFFFF;
      }
      &-desqr {
        font-size: 24px;
        color: #07166C;
        margin-top: 60px;
        line-height: 29px;
      }
      &-btns {
        margin-top: 25px;
      }
    }
    &__images {
      display: inline-block;
      position: relative;
      &-icons {
        left: 19px;
        top: -357px;
        position: absolute;
      }
      &-robot {
        left: 112px;
        top: -272px;
        position: absolute;
      }
      &-bottom {
        left: 155px;
        top: 58px;
        position: absolute;
      }
    }
    &__second-button {
      display: inline-block;
      margin-left: 68px;
      font-size: 18px;
      font-weight: 700;
      color: $primary;
      a {
        color: $primary;
      }
    }
  }

  button {
    width: 225px;
    height: 54px;
  }
  .rectangle {
    height: 2px;
  }
</style>