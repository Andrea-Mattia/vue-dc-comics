<template>
  <section class="jumbotron">
      <div class="container">
        <h1>CONTENT GOES HERE</h1>
      </div>
  </section>
</template>

<script>
export default {
    name: 'MainContent',
}
</script>

<style scoped lang="scss">
@import '../styles/mixins';

.jumbotron {
  padding: 3rem;
  background-image: url('../assets/img/jumbotron.jpg');
  background-size: cover;
}

div.container {
  @include df('vertical');
  justify-content: flex-start;
}

h1 {
  background: #fff;
}

</style>