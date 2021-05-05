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
      <FooterSocials />
    </footer>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import MainContent from '@/components/MainContent.vue';
import Shop from '@/components/Shop.vue';
import MainFooter from '@/components/MainFooter.vue';
import FooterSocials from '@/components/FooterSocials.vue';

export default {
  name: 'App',
  components: {
    Header,
    MainContent,
    Shop,
    MainFooter,
    FooterSocials,
  }
}
</script>

<style lang="scss">

@import './styles/general';
@import './styles/utilities';

</style>
