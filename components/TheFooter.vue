<template lang="pug">
footer(class="footer")
  div(class="footer__body container")
    div(class="footer__info")
      VueLogo
      p Cтатьи о дизайне и искусстве, которые исследуют творческие вдохновения и актуальные тенденции, раскрывая мир эстетики и креативности
    div(class="footer__socials footer-socials")
      div(class="footer-socials__email")
        div(class="footer-socials__email-title") email
        div testblogsupport@gmail.com
      ul(class="footer-socials__links")
        li(class="footer-socials__link")
          a 
            svg(width="30" height="30" viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg")
              circle(cx="15" cy="15" r="15" fill="#FEFEFE")
              path(d="M30 15C30 6.75 23.25 0 15 0C6.75 0 0 6.75 0 15C0 22.5 5.4375 28.6875 12.5625 29.8125V19.3125H8.8125V15H12.5625V11.625C12.5625 7.875 14.8125 5.8125 18.1875 5.8125C19.875 5.8125 21.5625 6.1875 21.5625 6.1875V9.9375H19.6875C17.8125 9.9375 17.25 11.0625 17.25 12.1875V15H21.375L20.625 19.3125H17.0625V30C24.5625 28.875 30 22.5 30 15Z" fill="#1B1B1B")
        li(class="footer-socials__link")
          a 
            svg(width="30" height="30" viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg")
              circle(cx="15" cy="15" r="15" fill="#FEFEFE")
              path(d="M30 15C30 6.75 23.25 0 15 0C6.75 0 0 6.75 0 15C0 22.5 5.4375 28.6875 12.5625 29.8125V19.3125H8.8125V15H12.5625V11.625C12.5625 7.875 14.8125 5.8125 18.1875 5.8125C19.875 5.8125 21.5625 6.1875 21.5625 6.1875V9.9375H19.6875C17.8125 9.9375 17.25 11.0625 17.25 12.1875V15H21.375L20.625 19.3125H17.0625V30C24.5625 28.875 30 22.5 30 15Z" fill="#1B1B1B")
  SubscribeFormBlock
</template>

<style scoped lang="scss">
.footer {
  display: flex;
  flex-direction: column;
  row-gap: 70px;

  margin-top: 200px;
  border-top: 1px solid #8d959c;
  padding-top: 50px;

  &__body {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px;
  }

  &__info {
    display: flex;
    flex-direction: column;
    row-gap: 20px;
    max-width: 425px;

    color: #8d959c;
    font-size: 14px;
    line-height: 142.857%;
  }
}

.footer-socials {
  display: flex;
  flex-direction: column;
  row-gap: 25px;

  &__email-title {
    color: #8d959c;
    font-size: 14px;
    line-height: 142.857%;
  }

  &__links {
    display: flex;
    column-gap: 20px;
  }
}
</style>
