<template lang="pug">
div(class="subscribe-form__wrapper container")
  section(class="subscribe-form")
    h2(class="subscribe-form__title") Подпишись на рассылку
    form(class="subscribe-form__form" @submit.prevent)
      input(class="subscribe-form__input input" placeholder="Email")
      button(class="subscribe-form__button button") Подписаться
</template>

<style scoped lang="scss">
.subscribe-form {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;

  background: #1b1b1b;
  color: #fefefe;
  padding: 35px 30px;
  flex-wrap: wrap;

  &__title {
    font-size: 22px;
    font-weight: 800;
    line-height: 136.364%;
  }

  &__form {
    display: flex;
    column-gap: 35px;
    row-gap: 10px;

    @media (max-width: 768px) {
      flex-wrap: wrap;
      width: 100%;
    }
  }

  &__input {
    width: 353px;

    @media (max-width: 768px) {
      width: 100%;
    }
  }

  &__button {
    @media (max-width: 768px) {
      width: 100%;
    }
  }
}
</style>
