<template>
  <form action class="contact-form">
    <input
      type="text"
      name="name"
      id="name"
      placeholder="Name:"
      required
      class="contact-form__input"
    />
    <input
      type="email"
      name="email"
      id="email"
      placeholder="Email:"
      required
      class="contact-form__input"
    />
    <textarea
      name="message"
      id="message"
      rows="6"
      placeholder="Message:"
      required
      class="contact-form__input"
    ></textarea>
    <button type="submit" class="btn btn--prime">Send</button>
  </form>
</template>

<style lang="scss" scoped>
@import "~@/assets/styles/vars";

.contact-form {
  padding: 0 30px 60px;

  &__input {
    width: 100%;
    margin-bottom: 18px;
    padding: 24px 15px 24px 30px;
    font-size: 22px;
    font-family: $f-text;
    background-color: #000;
    color: $c-text;
    border: none;
    outline: none;
    &::placeholder {
      color: $c-text-alt;
      opacity: 1; /* Firefox */
    }
  }

  @media (min-width: $sm) {
    flex: 1 1 55%;
  }
  @media (min-width: $lg) {
    order: 3;
    flex: 0 0 31%;
    padding: 0;
    margin-left: -60px;
  }
  @media (min-width: $xlg) {
    padding: 0;
    margin-left: -135px;
  }
}
</style>