<template>
  <main class="main-content contact">
    <img src="@/assets/img/map-wide.png" alt="Map with our location" class="contact__img" />

    <!-- <picture>
      <source srcset="../assets/img/map-mobile.png" media="(max-width: 1279px" ) />
      <source srcset="../assets/img/map-wide.png" media="(min-width: 1280px" ) />
    </picture>-->

    <div class="contact__content">
      <div class="title-box title-box--contact">
        <h1 class="title-box__title title-box__title--big">Contact</h1>
        <svg
          width="78"
          height="78"
          xmlns="http://www.w3.org/2000/svg"
          version="1.1"
          class="title-box__border title-box__border--right"
        >
          <rect width="72" height="72" x="3" y="3" />
        </svg>
      </div>
      <p class="contact__text">
        + 381 63 89 79 099
        <br />sanja@pickled-brain.com
      </p>
      <p class="contact__text">
        <a href="#" title="Find us on map" class="contact__text--address">
          Pariska 13
          <img src="@/assets/img/map-icon.png" alt="Map icon" width="25" height="22" />
        </a>
        <br />11000 Belgrade, Serbia
      </p>
    </div>
    <ContactForm />
  </main>
</template>

<script>
import ContactForm from "@/components/ContactForm.vue";

export default {
  components: {
    ContactForm
  }
};
</script>
<style lang="scss" scoped>
@import "~@/assets/styles/vars";
.contact {
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
    padding-bottom: 40px;
    font-size: 26px;
    &--address {
      font-weight: bold;
      text-decoration: underline;
      color: $c-text;
    }
  }

  @media (min-width: $sm) {
    @include flexCenter();
    flex-wrap: wrap;

    &__img {
      box-shadow: 0 0 59px 0 #0a0a0a;
      flex: 1 1 100%;
    }
    &__content {
      flex: 1 1 45%;
    }
  }

  @media (min-width: $lg) {
    flex-wrap: nowrap;
    max-width: 1225px;
    margin: 0 auto;
    &__img {
      order: 2;
      max-height: none;
      width: 550px;

      height: 550px;
    }
    &__content {
      order: 1;
      flex: 0 0 31%;
      padding: 0;
      margin-right: -60px;
      text-align: right;
      z-index: 10;
    }
  }
  @media (min-width: $xlg) {
    &__img {
      width: 100%;
      height: auto;
    }
    &__content {
      margin-right: -80px;
      justify-content: flex-end;
    }
    &__text {
      font-size: 32px;
    }
  }
}
</style>
