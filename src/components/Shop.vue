<template>
  <section class="shop">
      <div class="container">
          <ul>
              <li v-for="(link, index) in shopLinks" :key="index">
                  <a class="ttu" :href="link.url">
                      <img :src="link.img" :alt="link.text">
                      <span>{{ link.text }}</span>
                  </a>
              </li>
          </ul>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Shop',
    data() {
        return {
            shopLinks: [
                { text: 'digital comics', url: '/digitalcomics', img: require('../assets/img/buy-comics-digital-comics.png'), },
                { text: 'cd merchandise', url: '/cdmerchandise', img: require('../assets/img/buy-comics-merchandise.png'), },
                { text: 'subscription', url: '/subscription', img: require('../assets/img/buy-comics-subscriptions.png'), },
                { text: 'comic shop locator', url: '/comicshoplocator', img: require('../assets/img/buy-comics-shop-locator.png'), },
                { text: 'dc power visa', url: '/dcpowervisa', img: require('../assets/img/buy-dc-power-visa.svg'), },
            ],
        }
    },
}
</script>

<style scoped lang="scss">
@import '../styles/vars';
@import '../styles/mixins';

.shop {
    background: $brand-color;
    padding: 50px 0;
}

div.container {
    @include df();
}

ul {
    @include df();
}

li {
    a {
        @include df();
        min-width: 230px;
        color: $transparent-links;
        transition: transform .3s, color .3s; 
        &:hover {
            color: #fff;
            transform: scale(1.14);
            font-weight: bold;
        }
        & img {
            height: 50px;
            margin-right: 0.5rem;
        }
    }
}

li:last-child a img {
    height: 40px;
}

</style>