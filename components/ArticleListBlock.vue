<script setup>
const props = defineProps({
  data: Object,
});

const visibleArticles = ref(props.data.articles.slice(0,3))
</script>

<template lang="pug">
section(class="article-list container")
  h2(class="article-list__title") {{ data.title }}
  div(class="article-list__list")
    div(class="article-list__item article" v-for="article in visibleArticles")
      div(class="article__body")
        img(class="article__image" :src="article.image")
        h3(class="article__title") {{ article.title ?? null }}
      div(class="article__buttons")
        NuxtLink(class="article__button button-black" :to="article.link") Читать
</template>

<style scoped lang="scss">
.article-list {
  display: flex;
  flex-direction: column;
  row-gap: 50px;

  &__title {
    font-size: 22px;
    font-weight: 800;
    line-height: 136.364%;
  }

  &__list {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
  }
}
.article {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  row-gap: 30px;
  flex: 1 1 425px;

  &__image {
    width: 100%;
    height: 320px;
    object-fit: cover;
  }

  &__body {
    display: flex;
    flex-direction: column;
    row-gap: 20px;
  }

  &__buttons {
    display: flex;
  }
}
</style>
