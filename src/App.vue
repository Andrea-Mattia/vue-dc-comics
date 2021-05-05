<template>
  <div id="app">
    <!-- HEADER -->
    <Header />

    <!-- MAIN CONTENT -->
    <main>
      <MainContent />
      <Shop />
    </main>

    <!-- FOOTER -->
    <footer>
      <MainFooter />
    </footer>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import MainContent from '@/components/MainContent.vue'
import Shop from '@/components/Shop.vue'
import MainFooter from '@/components/MainFooter.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainContent,
    Shop,
    MainFooter,
  }
}
</script>

<style>
/* GENERAL */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  font-size: 14px;
}

/* UTILITIES */
img {
  max-width: 100%;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
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

.ttu {
  text-transform: uppercase;
}

</style>
