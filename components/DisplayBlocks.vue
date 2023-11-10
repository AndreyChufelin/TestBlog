<script setup>
const route = useRoute();

const { data } = await useFetch(
  () => "https://devtwit8.ru/api/v1/page/?path=" + route.path
);

const blocks = {
  article_list_block: resolveComponent("ArticleListBlock"),
  subscribe_form_block: resolveComponent("SubscribeFormBlock"),
  image_block: resolveComponent("ImageBlock"),
  article_intro_block: resolveComponent("ArticleIntroBlock"),
  cta_form_block: resolveComponent("CtaFormBlock"),
  text_block: resolveComponent("TextBlock"),
  slider_block: resolveComponent("SliderBlock"),
};

watch(route, () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
});
</script>

<template lang="pug">
Head
  Title {{ data?.meta?.title ?? "TestBlog"}}
template(v-if="data?.body")
  template(v-for="block in data.body")
    component( :is="blocks[block.type]" :data="block.data")
p(class="container" v-else) Page not found
</template>

<style lang="scss" scoped></style>
