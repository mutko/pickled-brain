<template>
  <!-- main-content -->
  <main class="main-content landing">
    <h1 class="landing__title">
      Pickled
      <br />brain
      <br />tattoo
      <!--
        P
        <span class="index-over">i</span>c
        <span class="index-over">k</span>led
        <br />bra
        <span class="index-over">i</span>n
        <br />t
        <span class="index-over">a</span>ttoo
      -->
    </h1>

    <div class="landing__box">
      <img
        src="@/assets/img/logo.png"
        width="87"
        height="144"
        alt="Pickled brain logo"
        class="landing__logo"
      />
      <p class="landing__subtitle">
        Belgrade
        <br />Serbia
      </p>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@import "~@/assets/styles/vars";
.landing {
  @include flexCenter();
  flex-direction: column;
  justify-content: center;
  position: relative;

  &__title {
    font-family: $f-title;
    line-height: 0.73;
    font-size: 74px;
    text-align: center;
    color: #000;
    position: absolute;
  }
  &__box {
    width: 178px;
    height: 380px;
    border: 7px solid $c-main;
    @include flexCenter();
    flex-direction: column;
  }
  &__logo {
    position: relative;
    top: -50px;
  }
  &__subtitle {
    color: $c-main;
    font-family: $f-title;
    font-size: 16px;
    align-self: flex-start;
    margin-top: auto;
    padding-left: 12px;
    padding-bottom: 16px;
  }

  @media (min-width: $sm) {
    margin-top: 180px;
    justify-content: flex-start;

    &__title {
      font-size: 114px;
      top: 114px;
    }
    &__box {
      height: 456px;
    }
    &__subtitle {
      font-size: 18px;
    }
  }
  @media (min-width: $lg) {
    margin-top: 60px;
    align-items: flex-start;

    &__title {
      text-align: left;
      font-size: 140px;
    }
    &__box {
      margin-left: 107px;
      width: 195px;
      height: 506px;
    }
    &__subtitle {
      font-size: 24px;
      align-self: flex-end;
      padding-left: 0;
      margin-right: -147px;
    }
  }
  @media (min-width: $xlg) {
    position: relative;
    &__title {
      font-size: 225px;
    }
    &__box {
      width: 310px;
      height: 682px;
      margin-left: 172px;
      z-index: 10;
    }
    &__logo {
      display: inline-block;
      width: 111px;
      height: 187px;
      top: 229px;
    }
    &__subtitle {
      font-size: 26px;
      margin-right: -150px;
    }
  }
}
</style>
