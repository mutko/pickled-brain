<template>
  <footer class="page-footer">
    <ul class="social-list">
      <li class="social-list__link social-list__link--fb">
        <a href="#" class="social-list__item" title="FB page">
          <img src="@/assets/img/fb.png" alt="Facebook icon" width="16" height="29" />
        </a>
      </li>
      <li class="social-list__link social-list__link--in">
        <a href="#" class="social-list__item" title="Instagram">
          <img src="@/assets/img/in.png" alt="Instagram icon" width="26" height="26" />
        </a>
      </li>
      <li class="social-list__link social-list__link--lang">
        <a href="#" class="social-list__item" title="Change language">
          <img src="@/assets/img/en.png" alt="Language flag" width="26" height="26" />
        </a>
      </li>
    </ul>
  </footer>
</template>

<style lang="scss" scoped>
@import "~@/assets/styles/vars";
.page-footer {
  padding: 0 30px 24px;

  @media (min-width: $sm) {
    padding-bottom: 36px;
  }
  @media (min-width: $lg) {
    padding: 0 0 75px;
  }
}
.social-list {
  @include flexCenter();

  &__link {
    &--fb {
      padding-right: 17px;
    }
    &--lang {
      margin-left: auto;
    }
  }

  &__item {
    display: block;
    line-height: 0;
  }

  @media (min-width: $sm) {
    justify-content: flex-end;
    &__link {
      &--fb {
        padding-right: 24px;
        img {
          width: 22px;
          height: 40px;
        }
      }
      &--in {
        img {
          width: 36px;
          height: 36px;
        }
      }
      &--lang {
        display: none;
      }
    }
  }
}
</style>