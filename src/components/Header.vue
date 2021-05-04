<template>
    <header class="df container">
        <a class="brand-logo" href="#">
            <img src="../assets/img/dc-logo.png" alt="dc-logo-header">
        </a>

        <nav>
            <ul class="df">
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
    min-height: 100px;
}

.brand-logo img {
    height: 80px;
}

li a {
    color: #000;
    padding: 38px 0.5rem;
}

li a.active,
li a:hover {
    border-bottom: 4px solid #1181e8;
}

</style>