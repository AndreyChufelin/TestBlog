<script setup>
const props = defineProps({
  data: String,
});
</script>

<template lang="pug">
section(class="text-block" v-html="data")
</template>

<style lang="scss">
.text-block {
  display: flex;
  flex-direction: column;
  row-gap: 20px;
  max-width: 884px;
  width: 100%;
  margin: 0 auto;
  padding: 10px;
  box-sizing: border-box;

  & h2 {
    font-size: 22px;
    font-weight: 800;
    line-height: 136.364%;
  }

  & ul {
    width: 70;
    margin: 0 auto;
  }

  & li {
    list-style: url("/icon-list-item.svg");
  }

  & blockquote {
    color: #1b1b1b;
    position: relative;
    font-style: italic;
    font-weight: 300;

    & p {
      margin-left: 116px;
    }

    & footer {
      color: #8d959c;
      font-size: 14px;
      font-weight: 400;
      font-style: normal;
      line-height: 142.857%;
      margin-left: 116px;
    }

    &:before {
      display: block;
      position: absolute;
      content: "";
      width: 80px;
      height: 64px;
      background: center / contain no-repeat url("/icon-quotes.svg");
    }
  }
}
</style>
