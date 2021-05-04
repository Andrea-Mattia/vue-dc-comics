<template>
  <section class="jumbotron">
      <div class="container df">
        <h1>CONTENT GOES HERE</h1>
      </div>
  </section>
</template>

<script>
export default {
    name: 'MainContent',
}
</script>

<style scoped>

.jumbotron {
  padding: 3rem;
  background-image: url('../assets/img/jumbotron.jpg');
  background-size: cover;
}

div.container {
  justify-content: flex-start;
}

h1 {
  background: #fff;
}

</style>