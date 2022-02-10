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
        <div class="check__content-search-input">
          <span class="check__content-search-input-text">Enter Instagram account...</span>
        </div>
        <div class="check__content-search-btn">
          <a href="#"><span class="check__content-search-btn-text">PREVIEW GROWTH</span></a>
        </div>
      </div>
      <div class="check__content-bottom">
        <p>Up to <span>15x</span> more effective than Instagram Bots</p>
      </div>
    </div>
    <div class="check__images">
      <img class="check__images-robot" src="../images/check-robot.png" alt="robot">
      <img class="check__images-phone" src="../images/check-phone.png" alt="phone">
      <img class="check__images-bottom" src="../images/check-background.png" alt="bottom">
    </div>
  </div>
</template>

<script>

export default {
  name: "Check",
}
</script>

<style lang="scss" scoped>
  .check {
    &__wrapper {
      height: 500px;
      margin: 0 141px;
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
          &-text {
            position: absolute;
            white-space: nowrap;
            top: 17px;
            left: 23px;
            color: #B5B5B5;
            font-size: 18px;
            &:before {
              content: url("../icons/check-insta.png");
              transform: translate(-2px, -5px);
              width: 32px;
              height: 32px;
              margin-right: 24px;
              vertical-align: -50%;
            }
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