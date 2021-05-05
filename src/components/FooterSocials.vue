<template>
  <section class="footer-social">
      <div class="container">
          <div>
              <button class="btn ttu">sign-up now!</button>
          </div>
          <div class="link-list">
              <h3 class="ttu">follow us</h3>
              <ul>
                  <li v-for="(link, index) in socialLinks" :key="index">
                      <a :href="link.url" target="_blank">
                          <img :src="link.src" :alt="link.alt">
                      </a>
                  </li>
              </ul>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'FooterSocials',
    data() {
        return {
            socialLinks: [
                {
                    url: 'https://www.facebook.com',
                    src: require('../assets/img/footer-facebook.png'),
                    alt: 'Facebook',
                },
                {
                    url: 'https://www.twitter.com',
                    src: require('../assets/img/footer-twitter.png'),
                    alt: 'Twitter',
                },
                {
                    url: 'https://www.youtube.com',
                    src: require('../assets/img/footer-youtube.png'),
                    alt: 'YouTube',
                },
                {
                    url: 'https://www.pinterest.com',
                    src: require('../assets/img/footer-pinterest.png'),
                    alt: 'Pinterest',
                },
                {
                    url: 'https://www.periscope.com',
                    src: require('../assets/img/footer-periscope.png'),
                    alt: 'Periscope',
                },
            ],
        }
    },
}
</script>

<style scoped lang="scss">
@import '../styles/vars';
@import '../styles/mixins';

.footer-social {
    background: #303030;
}

div.container {
    @include df('vertical');
    height: 100px;
    justify-content: space-between;
}

.btn {
    padding: 0.5rem;
    color: $transparent-links;
    font-weight: bold;
    background: transparent;
    border: 2px solid $brand-color;
    cursor: pointer;
    transition: transform .3s, color .3s;
    &:hover {
        transform: scale(1.15);
        color: #fff;
    }
}

.link-list {
    @include df();
}

ul {
    @include df();
    margin-left: 2rem;
    li a {
        margin-right: 1rem;
        text-decoration: none;
        img {
            transition: transform .3s;
            &:hover {
                transform: scale(1.15);
            }
        }
    }
}

h3 {
    color: $brand-color;;
}

</style>