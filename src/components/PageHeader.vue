<template>
  <header class="page-header">
    <nav class="page-nav">
      <ul class="page-nav__list">
        <li class="page-nav__item">
          <router-link to="/about" title="About us" class="page-nav__link">About</router-link>
        </li>
        <li class="page-nav__item">
          <router-link to="/gallery" title="Check our work" class="page-nav__link">Gallery</router-link>
        </li>
        <!-- <li class="page-nav__item">
          <a href="#" class="page-nav__link" title="Guides">Guides</a>
        </li>-->
        <li class="page-nav__item">
          <router-link to="/contact" title="Contact us" class="page-nav__link">Contact</router-link>
        </li>
        <li class="page-nav__item">
          <a href="#" class="page-nav__link page-nav__link--lang" title="Change language">
            <img src="@/assets/img/en.png" alt="Language flag" width="45" height="44" />
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
@import "~@/assets/styles/vars";
.page-header {
  display: none;

  @media (min-width: $sm) {
    display: block;
    padding-top: 64px;
  }
  @media (min-width: $sm) {
    padding-top: 64px;
  }
  @media (min-width: $sm) {
    padding-top: 72px;
  }
}
.page-nav {
  &__list {
    @include flexCenter();
  }
  &__item:last-child {
    line-height: 0;
  }
  &__link {
    display: inline-block;
    padding: 10px;
    color: $c-text;
    text-transform: uppercase;
    font-size: 18px;
    font-family: $f-strong;

    &--lang {
      padding: 0 0 0 20px;
    }
  }

  @media (min-width: $sm) {
    &__list {
      justify-content: center;
    }
    &__link {
      font-size: 24px;
    }
  }
  @media (min-width: $lg) {
    margin-right: -70px;

    &__list {
      justify-content: flex-end;
    }
    &__item--active {
      border: 3px solid $c-main;
    }
  }
}
</style>