<template>
  <div id="app">
    <!-- HEADER -->
    <Header />

    <!-- MAIN CONTENT -->
    <main>
      <MainContent />
    </main>

    <!-- FOOTER -->
    <footer>
      footer here
    </footer>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import MainContent from '@/components/MainContent.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainContent,
  }
}
</script>

<style>

  /* UTILITIES */
  img {
    max-width: 100%;
  }

  .df {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
  }

</style>
