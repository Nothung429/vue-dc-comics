<template>
    <main>
        <div class="wip__bg">
            <div class="frame">
                <div class="wip">
                    <h3>--> Content go here --></h3>
                </div>
            </div>
        </div>
        <div class="main__nav__bg">
            <div class="frame">
                <div class="main__nav">
                    <ul>
                        <li v-for="(link, index) in links" :key="index" :class="{active : link.current}">
                            <img :src="link.img" alt="main-li-img">
                            <a :href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
            </div>
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
                        img: require("../assets/img/buy-comics-digital-comics.png"),
                        current: false,
                    },
                    {
                        text: "dc merchandise",
                        url: "#",
                        img: require("../assets/img/buy-comics-merchandise.png"),
                        current: true,
                    },
                    {
                        text: "subscription",
                        url: "#",
                        img: require("../assets/img/buy-comics-subscriptions.png"),
                        current: false,
                    },
                    {
                        text: "comic shop location",
                        url: "#",
                        img: require("../assets/img/buy-comics-shop-locator.png"),
                        current: false,
                    },
                    {
                        text: "dc power visa",
                        url: "#",
                        img: require("../assets/img/buy-dc-power-visa.svg"),
                        current: false,
                    },
                ],
            }
        },
    }
</script>

<style lang="scss">
    .wip__bg {
        background-color: #1c1c1c;
    }
    .wip {
        height: 172px;
        h3 {
            text-align: center;
            line-height: 172px;
            color: #fff;
        }
    }
    .main__nav__bg {
        background-color: #0282f9;
    }
    .main__nav {
        display: flex;
        justify-content: center;
        & ul {
            display: flex;
            justify-content: center;
            & li {
            padding: 40px 10px;
            display: flex;
            align-items: center;
                a {
                    text-transform: uppercase;
                    color: #fff;
                }
                img {
                    margin-right: 10px;
                }
            }
        }
    }
</style>