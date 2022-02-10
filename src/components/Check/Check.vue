<template>
  <div class="check__wrapper" id="check">
    <div class="check__content-wrapper">
      <div class="check__content-header">
        <p class="check__content-header-header">Check Your Growth</p>
        <div class="check__content-header-group">
          <GradientRectangle></GradientRectangle>
          <p class="check__content-header-desqr">See your account after 30 days with Insocial</p>
        </div>
      </div>
      <div class="check__content-search">
        <input type="text" class="check__content-search-input" placeholder="Enter Instagram account...">
        <div class="check__content-search-btn">
          <a href="#"><span class="check__content-search-btn-text">PREVIEW GROWTH</span></a>
        </div>
      </div>
      <div class="check__content-bottom">
        <p>Up to <span>15x</span> more effective than Instagram Bots</p>
      </div>
    </div>
    <div class="check__images">
      <img class="check__images-robot" src="../../images/check-robot.png" alt="robot">
      <img class="check__images-phone" src="../../images/check-phone.png" alt="phone">
      <img class="check__images-bottom" src="../../images/check-background.png" alt="bottom">
    </div>
  </div>
</template>

<script>
import CustomButton from "@/components/UI/CustomButton";

export default {
  name: "Check",
  components: {
    CustomButton
  }
}
</script>

<style lang="scss" scoped>
  .check {
    &__wrapper {
      height: 500px;
      margin: -1px 141px 0;
    }
    &__content {
      &-header {
        margin-top: 10px;
        &-header {
          margin-top: 204px;
          font-size: 36px;
          font-weight: 600;
          color: $primary;
        }
        &-group {
          width: 393px;
          font-size: 18px;
        }
        &-desqr {
          margin-top: 3px;
        }
      }
      &-search {
        margin-top: 40px;
        display: flex;
        &-input {
          display: inline-block;
          width: 370px;
          height: 70px;
          border: 2px solid $primary;
          border-radius: 16px 0 0 16px;
          position: relative;
          background-image: url("../../icons/check-insta.png");
          background-repeat: no-repeat;
          background-position: 22px 17px;
          padding-left: 79px;
          font-size: 18px;
          color: #B5B5B5;
          &:focus {
            color: black
          }
        }
        &-btn {
          display: inline-block;
          width: 230px;
          height: 70px;
          border: 2px solid $primary;
          border-left: 0;
          border-radius: 0 16px 16px 0;
          background: #38D89A;
          position: relative;
          &-text {
            color: $primary;
            position: absolute;
            white-space: nowrap;
            top: 50%;
            left: 50%;
            text-align: center;
            font-weight: bold;
            font-size: 18px;
            transform: translate(-50%, -50%);
          }
        }
      }
      &-bottom {
        font-size: 18px;
        margin-top: 14px;
        & span {
          font-weight: bold;
          color: $primary;
        }
      }
    }
    &__images {
      position: relative;
      &-robot, &-phone, &-bottom {
        position: absolute;
      }
      &-robot {
        right: -24px;
        bottom: 213px;
        z-index: 10;
      }
      &-phone {
        right: 162px;
        bottom: -159px;
      }
      &-bottom {
        right: 65px;
        bottom: -194px;
        z-index: -10;
      }
    }
  }

.rectangle {
  height: 4px;
  margin-top: 1px;
}

</style>