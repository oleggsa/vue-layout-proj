<template>
  <div class="feedback__wrapper">
    <div class="feedback__content">
      <div class="feedback__content-header">
        <p>Case Studies</p>
        <GradientRectangle></GradientRectangle>
      </div>
      <div class="feedback__content-deqsr">
        <p>Our Instagram marketing services are made for growth.<br>
          Must-have for business, influencers, digital marketing specialists</p>
      </div>
      <div class="feedback__user">
        <div class="feedback__user-photo">
          <img src="../../images/case-photo.png" alt="profile photo">
        </div>
        <div class="feedback__user-info">
          <div class="feedback__user-info-name">Xena_axyenna</div>
          <div class="feedback__user-info-date">Odessa, Ukraine | January 2021</div>
          <div class="feedback__user-info-rate">
            <img src="../../icons/star.png" alt="star" v-for="item of 5">
          </div>
          <div class="feedback__user-info-text">
            You can spend thousands of dollars on ads or<br>
            buying followers to try and build a meaningful<br>
            audience on Instagram before seeing that it’s a<br>
            complete waste
          </div>
        </div>
      </div>
      <CustomButton>GET STARTED</CustomButton>
    </div>
    <div class="feedback__images">
      <div class="feedback__images-phone"><img src="../../images/case-phone.png" alt="phone"></div>
      <div class="feedback__images-bottom"><img src="../../images/case-bottom.png" alt="bottom"></div>
      <div class="feedback__images-robot"><img src="../../images/case-robot.png" alt="robot"></div>
    </div>
  </div>
</template>

<script>
import GradientRectangle from "@/components/UI/GradientRectangle";
import CustomButton from "@/components/UI/CustomButton";

export default {
  name: "index",
  components: {GradientRectangle, CustomButton}
}
</script>

<style lang="scss" scoped>
@import "../../assets/variables";

.feedback {
  &__wrapper {
    height: 700px;
    margin: 37px 140px 0;
  }
  &__content {
    &-header {
      display: inline-block;
      font-weight: 600;
      font-size: 36px;
      color: $primary;
    }
    &-deqsr {
      margin-top: 3px;
      font-size: 18px;
      color: $primary;
    }
  }
  &__user {
    &-photo {
      margin-top: 36px;
      margin-left: 173px;
    }
    &-info {
      margin-left: 109px;
      margin-top: 25px;
      &-name {
        font-weight: 600;
        font-size: 16px;
        color: #222222;
      }
      &-date {
        margin-top: 4px;
        font-size: 18px;
        color: #696969;
      }
      &-rate {
        margin-left: 2px;
        & img {
          display: inline-block;
          margin-top: 7px;
          margin-right: 7px;
        }
      }
      &-text {
        margin-top: 14px;
        font-weight: 500;
        font-size: 14px;
        color: #222222;
        text-transform: capitalize;
        line-height: 150%;
      }
    }
  }
  &__images {
    &-phone {
      position: relative;
      right: -739px;
      top: -490px;
    }
    &-bottom {
      position: relative;
      right: -631px;
      top: -579px;
      z-index: -2;
    }
    &-robot {
      position: relative;
      right: -746px;
      top: -1162px;
    }
  }
}

.rectangle {
  height: 4px;
}

.button-success {
  width: 225px;
  height: 54px;
  margin-top: 19px;
  margin-left: 178px;
}
</style>