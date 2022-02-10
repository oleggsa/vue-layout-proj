<template>
  <div class="why__wrapper" id="why">
    <div class="why__content-wrapper">
      <div class="why__content-header">
        <h1>Why INSOCIAL?</h1>
        <GradientRectangle/>
      </div>
      <p class="why__content-desqr">Our Instagram marketing services are made for growth.<br>
        Must-have for business, influencers, digital marketing specialists</p>
      <div class="why__content-btn-group">
        <WhyButton>
          <h4>AUTO PROMOTION</h4>
        </WhyButton>
        <WhyButtonActive>
          <h4>AUTO LIKING</h4>
          <p>Liking other people's posts</p>
        </WhyButtonActive>
        <WhyButton>
          <h4>DIRECT MESSAGES</h4>
        </WhyButton>
        <WhyButton>
          <h4>SCHEDULE POSTING</h4>
        </WhyButton>
        <WhyButton>
          <h4>COMMENT TRACKER</h4>
        </WhyButton>
        <WhyButton>
          <h4>HASHTAG GENERATOR</h4>
        </WhyButton>
      </div>
      <div class="why__images">
        <img src="../../images/why-phone.png" alt="phone" class="why__images-phone">
      </div>
      <MyButton>GET STARTED</MyButton>
    </div>
  </div>
</template>

<script>


export default {
  name: "Why",

}
</script>

<style lang="scss" scoped>
.why {
  &__wrapper {
    height: 625px;
    background-image: url('../../images/why-background.png');
    background-repeat: no-repeat;
    background-position: center;
    background-position-y: 52px;
  }
  &__content {
    &-wrapper {
      width: 540px;
      margin: 0 140px;
      position: relative;
    }
    &-header {
      display: inline-block;
      & h1 {
        font-size: 36px;
        font-weight: 600;
        color: #07166C;
      }
    }
    &-desqr {
      margin-top: 3px;
      font-size: 18px;
      width: 600px;
      color: #07166C;
    }
    &-btn-group {
      margin-top: 36px;
      margin-left: 27px;
    }
    &-button {
      &:before{
        position: absolute;
        height: 37px;
        width: 37px;
        left: 36px;
        top: 4px;
        margin-right: 24px;
        vertical-align: -17px;
      }
      & h4 {
        position: absolute;
        top: 20px;
        left: 111px;
      }
      & p {
        position: absolute;
        top: 42px;
        transform: translate(0, -50%);
        margin-left: 112px;
        font-size: 14px;
      }
      &-active {
        & h4 {
          position: absolute;
          top: 9px;
          left: 111px;
        }
        & p {
          position: absolute;
          font-size: 14px;
          font-weight: 400;
          top: 34px;
          left: 111px;
        }
      }
      &:first-child:before {
        content: url('../../icons/why-1.png');
      }
      &:nth-child(2):before {
        content: url('../../icons/why-2.png');
      }
      &:nth-child(3):before {
        content: url('../../icons/why-3.png');
      }
      &:nth-child(4):before {
        content: url('../../icons/why-4.png');
      }
      &:nth-child(5):before {
        content: url('../../icons/why-5.png');
      }
      &:nth-child(6):before {
        content: url('../../icons/why-6.png');
      }
    }
  }
  &__images-phone {
    position: absolute;
    top: 126px;
    left: 740px;
  }
}

button {
  width: 240px;
  height: 55px;
  margin-top: 16px;
  margin-left: 170px;
}
.rectangle {
  height: 4px;
  margin-top: 2px;
}

</style>