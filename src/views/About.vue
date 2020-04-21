<template>
  <!-- about -->
  <main class="main-content about">
    <img src="@/assets/img/about.jpg" alt="About background image" class="about__img" />
    <div class="about__content">
      <div class="title-box">
        <svg
          width="78"
          height="78"
          xmlns="http://www.w3.org/2000/svg"
          version="1.1"
          class="title-box__border title-box__border--left"
        >
          <rect width="72" height="72" x="3" y="3" />
        </svg>
        <h1 class="title-box__title">About</h1>
      </div>
      <p class="about__text">
        Pickled Brain Tattoo studio is Sanja Tomaševic, born 1987. She is
        into tattoos for the last 10 years, and for the last 3 years - by
        profession.
      </p>
      <p class="about__text">
        There is a rich and versatile portfolio behind her, and you can get
        a glimps of it checking out this website (gallery above), or
        facebook page linked below.
      </p>
      <p class="about__text">Cheers, and see you at the studio</p>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@import "~@/assets/styles/vars";
.about {
  &__img {
    display: block;
    width: 100%;
    height: 375px;
    max-height: 400px;
    object-fit: cover;
  }
  &__content {
    padding: 0 30px;
  }
  &__text {
    padding-bottom: 20px;
    font-size: 19px;
    color: $c-text-alt;
  }
  @media (min-width: $sm) {
    padding: 0 94px;
    @include flexCenter();
    justify-content: center;
    &__img {
      width: 233px;
      height: 484px;
      max-height: none;
      box-shadow: 0 0 59px 0 #0a0a0a;
      object-position: 30% 0;
    }
    &__content {
      padding: 0;
      margin-left: 64px;
      flex: 0 254px;
    }
  }
  @media (min-width: $lg) {
    padding: 0;

    &__img {
      width: 297px;
      height: 452px;
    }
    &__content {
      margin-left: 78px;
      flex: 0 624px;
    }
    &__text {
      font-size: 23px;
    }
  }
}
</style>