<template>
    <footer>
        <div class="footer__nav__bg">
            <div class="frame">
                <div class="footer__nav">
                    <div class="links">
                        <div class="col-1">
                            <div class="link-group-1">
                                <h3>dc comics</h3>
                                <ul>
                                    <li v-for="(link, index) in group1links" :key="index" :class="{active : link.current}">
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
                        <div class="col-2">
                            <div class="link-group-2">
                                <h3>dc</h3>
                                <ul>
                                    <li v-for="(link, index) in group2links" :key="index" :class="{active : link.current}">
                                        <a :href="link.url">{{link.text}}</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        <div class="col-3">
                            <div class="link-group-3">
                                <h3>sites</h3>
                                <ul>
                                    <li v-for="(link, index) in group3links" :key="index" :class="{active : link.current}">
                                        <a :href="link.url">{{link.text}}</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>                    
                    <div class="footer__nav__img">
                        <img src="../assets/img/dc-logo-bg.png" alt="">
                    </div>
                </div>
            </div>            
        </div>

        <div class="footer__social__bg">
            <div class="frame">
                <div class="footer__social">
                    <div class="footer__social__btn">
                        <button>SIGN-UP NOW!</button>
                    </div>
                    <div class="footer__social__links">
                        <h3>FOLLOW US</h3>
                        <ul>
                            <li v-for="(link, index) in socialLinks" :key="index" :class="{active : link.current}">
                                <img :src="`link.img`" alt="footer-li-img">
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
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
                socialLinks: [
                    {
                        img: "../assets/img/footer-facebook.png",
                        url: "#",
                        current: true,
                    },
                    {
                        img: "../assets/img/footer-twitter.png",
                        url: "#",
                        current: true,
                    },
                    {
                        img: "../assets/img/footer-youtube.png",
                        url: "#",
                        current: true,
                    },
                    {
                        img: "../assets/img/footer-pinterest.png",
                        url: "#",
                        current: true,
                    },
                    {
                        img: "../assets/img/footer-periscope.png",
                        url: "#",
                        current: true,
                    },
                ],
            }
        },
    }
</script>

<style lang="scss" scoped>
    .footer__nav__bg {
        background-image: url("../assets/img/footer-bg.jpg");
        background-repeat: no-repeat;
        background-size: cover;
    }
    .footer__nav {
        display: flex;
        justify-content: space-between;
        height: 400px;
        .links {
            display: flex;
            padding: 80px 10px;
            gap: 20px;
            a {
                color: #959588;
            }
            .link-group-1 {
                margin-bottom: 20px;
            }
        }
        h3 {
            text-transform: uppercase;
            padding-bottom: 10px;
            color: #fff;
        }
        &__img {
            max-width: 400px;
            img {
                width: 100%;
            }
        }
    }
    .footer__social__bg {
        background-color: #303030;
    }
    .footer__social {
        display: flex;
        justify-content: space-between;
        align-content: center;
        height: 80px;
        &__btn {
            display: flex;
            justify-content: center;
            align-items: center;
            button {
                background-color: #303030;
                border: 2px solid #0282f9;
                color: #fff;
                font-size: 18px;
                padding: 10px 20px;
            }
        }
        &__links {
            display: flex;
            justify-content: center;
            align-items: center;
            h3 {
                padding-right: 20px;
                color: #0282f9;
            }
            ul {
                display: flex;
                justify-content: center;
                align-items: center;
                & li {
                    img {
                        width: 80px;
                        height: 80px;
                        margin-right: 10px;
                    }
                }
            }
        }
    }
</style>