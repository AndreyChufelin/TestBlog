<script setup>
const props = defineProps({
  data: Object,
});
</script>

<template lang="pug">
section(class="image-blocks container")
  img(class="image-blocks__image" :src="data.src")
  p(class="image-blocks__caption") {{ data.caption }}
</template>

<style scoped lang="scss">
.image-blocks {
  display: flex;
  flex-direction: column;
  row-gap: 15px;

  &__image {
    width: 100%;
    max-height: 560px;
    object-fit: cover;
    border-radius: 2px 220px 2px 2px;

    @media (max-width: 768px) {
      border-radius: 2px 120px 2px 2px;
    }
  }

  &__caption {
    color: #8d959c;
    text-align: right;
    font-size: 14px;
    line-height: 142.857%;
  }
}
</style>
