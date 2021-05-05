<template>
    <section class="main-footer">
        <div class="container df">
            <div class="footer-left df">
                <div>
                    <div class="dc-comics">
                        <h3 class="ttu">{{footerLinks[actualIndex].title}}</h3>
                        <ul>
                            <li v-for="(link, index) in footerLinks[actualIndex].links" :key="index">
                                <a href="#">{{link.text}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="shop">

                        <h3 class="ttu">{{footerLinks[actualIndex + 1].title}}</h3>
                        <ul>
                            <li v-for="(link, index) in footerLinks[actualIndex + 1].links" :key="index">
                                <a href="#">{{link.text}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="dc">
                    <h3 class="ttu">{{footerLinks[actualIndex + 2].title}}</h3>
                    <ul>
                        <li v-for="(link, index) in footerLinks[actualIndex + 2].links" :key="index">
                            <a href="#">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="sites">
                    <h3 class="ttu">{{footerLinks[actualIndex + 3].title}}</h3>
                    <ul>
                        <li v-for="(link, index) in footerLinks[actualIndex + 3].links" :key="index">
                            <a href="#">{{link.text}}</a>
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
                            url: '#',
                        },
                        {
                            text: 'Comics',
                            url: '#',
                        },
                        {
                            text: 'Movies',
                            url: '#',
                        },
                        {
                            text: 'TV',
                            url: '#',
                        },
                        {
                            text: 'Games',
                            url: '#',
                        },
                        {
                            text: 'Videos',
                            url: '#',
                        },
                        {
                            text: 'News',
                            url: '#',
                        },
                    ],
                },
                { 
                    title: 'shop',
                    links: [
                        {
                            text: 'Shop DC',
                            url: '#',
                        },
                        {
                            text: 'Shop DC Collectibles',
                            url: '#',
                        },
                    ],
                },
                { 
                    title: 'dc',
                    links: [
                        {
                            text: 'Termf Of Use',
                            url: '#',
                        },
                        {
                            text: 'Privacy policy (New)',
                            url: '#',
                        },
                        {
                            text: 'Ad Choices',
                            url: '#',
                        },
                        {
                            text: 'Advertising',
                            url: '#',
                        },
                        {
                            text: 'Jobs',
                            url: '#',
                        },
                        {
                            text: 'Subscriptions',
                            url: '#',
                        },
                        {
                            text: 'Talent Workshops',
                            url: '#',
                        },
                        {
                            text: 'CPSC Certificares',
                            url: '#',
                        },
                        {
                            text: 'Ratings',
                            url: '#',
                        },
                        {
                            text: 'Shop Help',
                            url: '#',
                        },
                        {
                            text: 'Contact Us',
                            url: '#',
                        },
                    ],
                },
                { 
                    title: 'sites',
                    links: [
                        {
                            text: 'DC',
                            url: '#',
                        },
                        {
                            text: 'MAD Magazine',
                            url: '#',
                        },
                        {
                            text: 'Dc Kids',
                            url: '#',
                        },
                        {
                            text: 'DC Universe',
                            url: '#',
                        },
                        {
                            text: 'DC Power Visa',
                            url: '#',
                        },
                    ],
                },
            ],
            actualIndex: 0,
        }
    },
}
</script>

<style scoped>

.main-footer {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
}

div.container {
    justify-content: space-between;
}

/* FOOTER LEFT */
.footer-left {
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
}

li a {
    font-size: 12px;
    color: rgba(255, 255, 255, .7);
    transition: color .3s;
}

li a:hover {
    color: #fff;
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