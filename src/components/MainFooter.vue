<template>
    <section class="main-footer">
        <div class="container">
            <div class="footer-left">
                <div>
                    <div class="dc-comics">
                        <h3 class="ttu">{{footerLinks[actualIndex].title}}</h3>
                        <ul>
                            <li v-for="(link, index) in footerLinks[actualIndex].links" :key="index">
                                <a :href="link.url">{{link.text}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="shop">
                        <h3 class="ttu">{{footerLinks[actualIndex + 1].title}}</h3>
                        <ul>
                            <li v-for="(link, index) in footerLinks[actualIndex + 1].links" :key="index">
                                <a :href="link.url">{{link.text}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="dc">
                    <h3 class="ttu">{{footerLinks[actualIndex + 2].title}}</h3>
                    <ul>
                        <li v-for="(link, index) in footerLinks[actualIndex + 2].links" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="sites">
                    <h3 class="ttu">{{footerLinks[actualIndex + 3].title}}</h3>
                    <ul>
                        <li v-for="(link, index) in footerLinks[actualIndex + 3].links" :key="index">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer-right">
                <img src="../assets/img/dc-logo-bg.png" alt="dc-logo-bg">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MainFooter',
    data() {
        return {
            footerLinks: [
                { 
                    title: 'dc comics',
                    links: [
                        {
                            text: 'Characters',
                            url: '/characters',
                        },
                        {
                            text: 'Comics',
                            url: 'comics',
                        },
                        {
                            text: 'Movies',
                            url: '/movies',
                        },
                        {
                            text: 'TV',
                            url: '/tv',
                        },
                        {
                            text: 'Games',
                            url: '/games',
                        },
                        {
                            text: 'Videos',
                            url: '/videos',
                        },
                        {
                            text: 'News',
                            url: '/news',
                        },
                    ],
                },
                { 
                    title: 'shop',
                    links: [
                        {
                            text: 'Shop DC',
                            url: '/shopdc',
                        },
                        {
                            text: 'Shop DC Collectibles',
                            url: '/shopdccollect',
                        },
                    ],
                },
                { 
                    title: 'dc',
                    links: [
                        {
                            text: 'Term Of Use',
                            url: '/termofuse',
                        },
                        {
                            text: 'Privacy policy (New)',
                            url: '/privacypolicy',
                        },
                        {
                            text: 'Ad Choices',
                            url: '/adchoices',
                        },
                        {
                            text: 'Advertising',
                            url: '/advertising',
                        },
                        {
                            text: 'Jobs',
                            url: '/jobs',
                        },
                        {
                            text: 'Subscriptions',
                            url: '/subscriptions',
                        },
                        {
                            text: 'Talent Workshops',
                            url: '/talentworkshop',
                        },
                        {
                            text: 'CPSC Certificates',
                            url: '/cpsccertificates',
                        },
                        {
                            text: 'Ratings',
                            url: '/ratings',
                        },
                        {
                            text: 'Shop Help',
                            url: '/shophelp',
                        },
                        {
                            text: 'Contact Us',
                            url: '/contactus',
                        },
                    ],
                },
                { 
                    title: 'sites',
                    links: [
                        {
                            text: 'DC',
                            url: '/dc',
                        },
                        {
                            text: 'MAD Magazine',
                            url: '/madmagazine',
                        },
                        {
                            text: 'Dc Kids',
                            url: '/dckids',
                        },
                        {
                            text: 'DC Universe',
                            url: '/dcuniverse',
                        },
                        {
                            text: 'DC Power Visa',
                            url: '/dcpowervisa',
                        },
                    ],
                },
            ],
            actualIndex: 0,
        }
    },
}
</script>

<style scoped lang="scss">
@import '../styles/vars';
@import '../styles/mixins';

.main-footer {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
}

div.container {
    @include df('vertical');
    justify-content: space-between;
}

/* FOOTER LEFT */
.footer-left {
    display: flex;
    width: 360px;
    padding: 2rem 0;
    justify-content: space-between;
    align-self: center;
    align-items: flex-start;
}

h3 {
    color: #fff;
}

ul {
    margin: 1rem 0;
}

li {
    padding: 2px 0;
    a {
        font-size: 12px;
        color: $transparent-links;
        transition: color .3s;
        &:hover {
            color: #fff;
        }
    }
}

/* FOOTER RIGHT */
.footer-right {
    height: 350px;
    overflow: hidden;
}

.footer-right img {
    transform: translateY(-100px);
}


</style>