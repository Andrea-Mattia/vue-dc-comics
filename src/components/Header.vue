<template>
    <header class="container">
        <a class="brand-logo" href="/home">
            <img src="../assets/img/dc-logo.png" alt="dc-logo-header">
        </a>

        <nav>
            <ul>
                <li v-for="(link, index) in headerLinks" :key="index">
                    <a class="ttu" :class="{active : link.current}" :href="link.url">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            headerLinks: [
                { text: 'characters', url: '/characters', current: false },
                { text: 'comics', url: '/comics', current: true },
                { text: 'movies', url: '/movies', current: false },
                { text: 'tv', url: '/tv', current: false },
                { text: 'games', url: '/games', current: false },
                { text: 'collectibles', url: '/collectibles', current: false },
                { text: 'videos', url: '/videos', current: false },
                { text: 'fans', url: '/fans', current: false },
                { text: 'news', url: '/news', current: false },
                { text: 'shop', url: '/shop', current: false },
            ],
        }
    },
}
</script>

<style scoped lang="scss">
@import '../styles/vars';
@import '../styles/mixins';

header.container {
    @include df('vertical');
    justify-content: space-between;
    min-height: 100px;
}

.brand-logo img {
    height: 80px;
}

ul {
    @include df();
}

li {
    a {
        color: #000;
        padding: 38px 0.5rem;
        border-bottom: 4px solid transparent;
        transition: border-color .3s;
        &.active,
        &:hover {
            border-bottom: 4px solid $brand-color;
        }
    }
}

</style>