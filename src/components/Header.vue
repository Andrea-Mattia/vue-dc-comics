<template>
    <header class="df container">
        <a href="#">
            <img src="../assets/img/dc-logo.png" alt="dc-logo-header">
        </a>

        <nav>
            <ul class="df">
                <li v-for="(link, index) in headerLinks" :key="index">
                    <a :class="{active : link.current}" :href="link.url">{{ link.text }}</a>
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
                { text: 'characters', url: '#', current: false },
                { text: 'comics', url: '#', current: true },
                { text: 'movies', url: '#', current: false },
                { text: 'tv', url: '#', current: false },
                { text: 'games', url: '#', current: false },
                { text: 'collectibles', url: '#', current: false },
                { text: 'videos', url: '#', current: false },
                { text: 'fans', url: '#', current: false },
                { text: 'news', url: '#', current: false },
                { text: 'shop', url: '#', current: false },
            ],
        }
    },
}
</script>

<style scoped>

    header.container {
        justify-content: space-between;
        min-height: 150px;
    }

    ul {
        list-style: none;
    }

    li a {
        text-transform: uppercase;
        text-decoration: none;
        color: #000;
        padding: 60px 0.5rem;
    }

    li a.active,
    li a:hover {
        border-bottom: 5px solid #1181e8;
    }

</style>