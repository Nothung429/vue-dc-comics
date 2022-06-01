<template>
    <footer>
        
        <div class="footer__nav">
            <div class="link-group-1">
                <h3>dc comics</h3>
                <ul>
                    <li v-for="(link, index) in group1links" :key="index" :class="{active : link.current}">
                        <a :href="link.url">{{link.text}}</a>
                    </li>
                </ul>
            </div>
            <div class="link-group-2">
                <h3>dc</h3>
                <ul>
                    <li v-for="(link, index) in group2links" :key="index" :class="{active : link.current}">
                        <a :href="link.url">{{link.text}}</a>
                    </li>
                </ul>
            </div>
            <div class="link-group-3">
                <h3>sites</h3>
                <ul>
                    <li v-for="(link, index) in group3links" :key="index" :class="{active : link.current}">
                        <a :href="link.url">{{link.text}}</a>
                    </li>
                </ul>
            </div>
            <div class="link-group-4">
                <h3>shop</h3>
                <ul>
                    <li v-for="(link, index) in group4links" :key="index" :class="{active : link.current}">
                        <a :href="link.url">{{link.text}}</a>
                    </li>
                </ul>
            </div>
        </div>

        <div class="footer__social">
            <div class="footer-btn">
                <button>sign up now</button>
            </div>
            <ul>
                <li v-for="(link, index) in sociallinks" :key="index" :class="{active : link.current}">
                    <img :src="link.img" alt="footer-li-img">
                </li>
            </ul>
        </div>

    </footer>
</template>

<script>
    export default {
        name: 'BaseFooter',
        data() {
            return {
                group1links: [
                    {
                        text: "Characters",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Comics",
                        url: "#",
                        current: true,
                    },
                    {
                        text: "Movies",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "TV",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Games",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Videos",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "News",
                        url: "#",
                        current: false,
                    },
                ],
                group2links: [
                    {
                        text: "Terms of Use",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Privacy policy(New)",
                        url: "#",
                        current: true,
                    },
                    {
                        text: "Ad Choices",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Advertising",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Jobs",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Subscriptions",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Talent Workshop",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "CPSC Certificates",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Ratings",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Shop Help",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Contact Us",
                        url: "#",
                        current: false,
                    },
                ],
                group3links: [
                    {
                        text: "DC",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "MAD Magazine",
                        url: "#",
                        current: true,
                    },
                    {
                        text: "DC Kids",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "DC Universe",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "DC Power Visa",
                        url: "#",
                        current: false,
                    },
                ],
                group4links: [
                    {
                        text: "Shop DC",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Shop DC Collectibles",
                        url: "#",
                        current: true,
                    },
                ],
                sociallinks: [
                    {
                        img: "../assets/img/buy-comics-merchandise.png",
                        url: "#",
                        current: true,
                    },
                    {
                        img: "../assets/img/buy-comics-merchandise.png",
                        url: "#",
                        current: true,
                    },
                    {
                        img: "../assets/img/buy-comics-merchandise.png",
                        url: "#",
                        current: true,
                    },
                    {
                        img: "../assets/img/buy-comics-merchandise.png",
                        url: "#",
                        current: true,
                    },
                    {
                        img: "../assets/img/buy-comics-merchandise.png",
                        url: "#",
                        current: true,
                    },
                ],
            }
        },
    }
</script>

<style>

</style>