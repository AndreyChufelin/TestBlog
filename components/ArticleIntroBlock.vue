<script setup>
defineProps({
  data: Object,
});
</script>

<template lang="pug">
section(class="intro container")
  img(class="intro__image" :src="data.image")
  div(class="intro__body")
    h2(class="intro__title") {{ data.title }}
    div(class="intro__info")
      div(class="intro__info-item") 
        svg(width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg")
          g(opacity="0.6")
            mask(id="mask0_5_530" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="1" y="1" width="14" height="14")
              path(d="M7.99994 13.6C11.0928 13.6 13.6 11.0929 13.6 8C13.6 4.9071 11.0928 2.39996 7.99994 2.39996C4.90704 2.39996 2.3999 4.9071 2.3999 8C2.3999 11.0929 4.90704 13.6 7.99994 13.6Z" fill="white" stroke="white" stroke-width="1.12001" stroke-linejoin="round")
              path(d="M8.0022 4.63997V8.00279L10.3763 10.3772" stroke="black" stroke-width="1.12001" stroke-linecap="round" stroke-linejoin="round")
            g(mask="url(#mask0_5_530)")
              path(d="M1.28003 1.27995H14.7201V14.72H1.28003V1.27995Z" fill="#8D959C")
        | {{ data.reading_time }} мин время чтения
      div(class="intro__info-item") 
        svg(width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg")
          g(opacity="0.6")
            path(d="M7.99996 6C7.46953 6 6.96082 6.21071 6.58575 6.58579C6.21067 6.96086 5.99996 7.46957 5.99996 8C5.99996 8.53043 6.21067 9.03914 6.58575 9.41421C6.96082 9.78929 7.46953 10 7.99996 10C8.53039 10 9.0391 9.78929 9.41417 9.41421C9.78925 9.03914 9.99996 8.53043 9.99996 8C9.99996 7.46957 9.78925 6.96086 9.41417 6.58579C9.0391 6.21071 8.53039 6 7.99996 6ZM7.99996 11.3333C7.1159 11.3333 6.26806 10.9821 5.64294 10.357C5.01782 9.7319 4.66663 8.88406 4.66663 8C4.66663 7.11595 5.01782 6.2681 5.64294 5.64298C6.26806 5.01786 7.1159 4.66667 7.99996 4.66667C8.88401 4.66667 9.73186 5.01786 10.357 5.64298C10.9821 6.2681 11.3333 7.11595 11.3333 8C11.3333 8.88406 10.9821 9.7319 10.357 10.357C9.73186 10.9821 8.88401 11.3333 7.99996 11.3333ZM7.99996 3C4.66663 3 1.81996 5.07333 0.666626 8C1.81996 10.9267 4.66663 13 7.99996 13C11.3333 13 14.18 10.9267 15.3333 8C14.18 5.07333 11.3333 3 7.99996 3Z" fill="#8D959C")
        | {{ data.views_count }} прочитали статью
    p(class="intro__description") {{ data.short_description }}
</template>

<style scoped lang="scss">
.intro {
  display: flex;
  gap: 30px;
  align-items: center;

  @media (max-width: 768px) {
    flex-wrap: wrap;
  }

  &__image {
    max-width: 541px;
    max-height: 580px;
    border-radius: 2px 220px 2px 2px;
    background: #d9d9d9;
    object-fit: cover;

    @media (max-width: 992px) {
      border-radius: 2px 120px 2px 2px;
      max-width: 320px;
      max-height: 320px;
    }
    @media (max-width: 768px) {
      max-width: 100%;
      width: 100%;
    }
  }

  &__body {
    margin-bottom: 40px;
  }

  &__title {
    font-size: clamp(24px, 5vw, 56px);
    font-weight: 800;
    line-height: 117.857%;
  }

  &__info {
    display: flex;
    flex-direction: column;
    row-gap: 4px;
    margin: 30px 0px 50px 0px;
  }

  &__info-item {
    display: flex;
    align-items: center;
    column-gap: 8px;
    color: #8d959c;
    font-size: 14px;
    line-height: 142.857%;
  }
}
</style>
