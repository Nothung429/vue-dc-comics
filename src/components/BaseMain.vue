<template>
    <main>
        <div class="wip">
            <h3>--> Content go here</h3>
        </div>
        <div class="main__nav">
            <ul>
                <li v-for="(link, index) in links" :key="index" :class="{active : link.current}">
                    <img :src="link.img" alt="main-li-img">
                    <a :href="link.url">{{link.text}}</a>
                </li>
            </ul>
        </div>
    </main>
</template>

<script>
    export default {
        name: 'BaseMain',
        data() {
            return {
                links: [
                    {
                        text: "digital comics",
                        url: "#",
                        img: "buy-comics-digital-comics.png",
                        current: false,
                    },
                    {
                        text: "dc merchandise",
                        url: "#",
                        img: "../assets/img/buy-comics-merchandise.png",
                        current: true,
                    },
                    {
                        text: "subscription",
                        url: "#",
                        img: "../assets/img/buy-comics-subscriptions.png",
                        current: false,
                    },
                    {
                        text: "comic shop location",
                        url: "#",
                        img: "../assets/img/buy-comics-shop-locator.png",
                        current: false,
                    },
                    {
                        text: "dc power visa",
                        url: "#",
                        img: "../assets/img/buy-dc-power-visa.png",
                        current: false,
                    },
                ],
            }
        },
    }
</script>

<style lang="scss">
    .wip {
        background-color: red;
        width: 100%;
        height: 100px;
    }
</style>