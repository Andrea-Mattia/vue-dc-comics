<template>
  <section class="shop">
      <div class="container df">
          <ul class="df">
              <li v-for="(link, index) in shopLinks" :key="index">
                  <a class="ttu df" :href="link.url">
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
                { text: 'digital comics', url: '#', img: require('../assets/img/buy-comics-digital-comics.png'), },
                { text: 'cd merchandise', url: '#', img: require('../assets/img/buy-comics-merchandise.png'), },
                { text: 'subscription', url: '#', img: require('../assets/img/buy-comics-subscriptions.png'), },
                { text: 'comic shop locator', url: '#', img: require('../assets/img/buy-comics-shop-locator.png'), },
                { text: 'dc power visa', url: '#', img: require('../assets/img/buy-dc-power-visa.svg'), },
            ],
        }
    },
}
</script>

<style scoped>
.shop {
    background: #1181e8;
    padding: 50px 0;
}

li:not(:last-child) {
    margin-right: 0.5rem;
}

li a {
    min-width: 230px;
    color: rgba(255, 255, 255, .7);
    transition: transform .3s, color .3s;
}

li a:hover {
    color: #fff;
    transform: scale(1.14);
    font-weight: bold;
}

li a img {
    height: 50px;
    margin-right: 0.5rem;
}

li:last-child a img {
    height: 40px;
}

</style>