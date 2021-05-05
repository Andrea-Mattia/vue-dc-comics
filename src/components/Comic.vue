<template>
  <div class="box">
      <img :src="details.thumb" :alt="details.series">
      <span class="ttu">{{ details.series }}</span>
  </div>
</template>

<script>
export default {
    name: 'Comic',
    props: {
        details: Object,
    },
}
</script>

<style scoped lang="scss">
@import '../styles/mixins';
@import '../styles/vars';

.box {
    @include df('horizontal');
    flex-direction: column;
    flex-basis: calc(100% / 6);
    margin: 2rem auto;
    padding: 0 1rem;
    cursor: pointer;
    transition: transform .3s;
    &:hover {
        transform: scale(1.15);
    }
    &:hover span {
        color: #fff;
    }
    span {
        margin-top: 1rem;
        color: $transparent-links;
        transition: color .3s;
    }
}
</style>