<template>
  <section>
    <div class="jumbotron"></div>
    <div class="content">
      <div class="container">
        <div class="current ttu">current series</div>
        <Comic v-for="(comic, index) in comics" 
              :key="index" 
              :details="comic" 
        />
        <div class="load ttu">load more</div>
      </div>
    </div>
  </section>
</template>

<script>
import DcComics from '@/data/dcComics.js';
import Comic from '@/components/Comic.vue';

export default {
    name: 'MainContent',
    components: {
      Comic,
    },
    data() {
      return {
        comics: DcComics,
      }
    },
}
</script>

<style scoped lang="scss">
@import '../styles/mixins';
@import '../styles/vars';

.jumbotron {
  height: 300px;
  background-image: url('../assets/img/jumbotron.jpg');
  background-size: cover;
}

.content {
  padding: 2rem;
  background: #1c1c1c;
}

div.container {
  @include df();
  position: relative;
  flex-wrap: wrap;
}

.current {
  position: absolute;
  bottom: 100%;
  left: 8%;
  padding: 0.8rem;
  background: $brand-color;
  color: #fff;
  font-weight: bold;
}

.load {
  padding: 0.8rem;
  background: $brand-color;
  color: $transparent-links;
  font-weight: bold;
  cursor: pointer;
  transition: transform .3s, color .3s;
  &:hover {
    transform: scale(1.15);
    color: #fff;
  }
}

</style>