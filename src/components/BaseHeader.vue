<template>
    <header>
        <div class="header__logo">
            <img src="../assets/img/dc-logo.png">
        </div>
        <div class="header__nav">
            <ul>
                <li v-for="(link, index) in links" :key="index" :class="{active : link.current}">
                    <a :href="link.url">{{link.text}}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    name: 'BaseHeader',
    data() {
        return {
            links: [
                {
                    text: "characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "games",
                    url: "#",
                    current: false,
                },
                {
                    text: "collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "news",
                    url: "#",
                    current: false,
                },
                {
                    text: "shop",
                    url: "#",
                    current: false,
                },
            ],
        }
    },
}
</script>

<style>
    
</style>