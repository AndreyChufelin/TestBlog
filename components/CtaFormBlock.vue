<script setup></script>

<template lang="pug">
div(class="cta-form__wrapper container")
  section(class="cta-form")
    img(class="cta-form__image" src="/cta-image.png")
    div(class="cta-form__body")
      h2(class="cta-form__title") Стань участником проекта
      form(class="cta-form__form" @submit.prevent="")
        div(class="cta-form__inputs")
          input(class="input" placeholder="Имя")
          input(class="input" placeholder="Телефон")
          input(class="input" placeholder="Email")
        div
          button(class="button") Присоединиться
</template>

<style scoped lang="scss">
.cta-form {
  background: #1b1b1b;
  display: flex;
  flex-wrap: wrap;
  gap: 60px;
  padding: 60px;

  &__image {
    flex: 1 1 100px;
    max-width: 100%;
    object-fit: cover;
  }

  &__title {
    color: #fefefe;
    font-size: 34px;
    font-weight: 800;
    line-height: 46px;
  }

  &__body {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    flex: 1 1 100px;
    gap: 50px;
  }

  &__inputs {
    display: flex;
    flex-direction: column;
    gap: 25px;
    max-width: 360px;
  }

  &__form {
    display: flex;
    flex-direction: column;
    gap: 50px;
  }
}
</style>
