<template>
    <main>
        <div class="main__jumbotron"></div>
        <div class="main__series">
            <div class="frame">
                <div class="main__series__note">
                    <h3>current series</h3>
                </div>
                <div class="main__series__comics">
                    <div class="main__series__comics__container" v-for="(comic, index) in comics" :key="index">
                        <img :src="comic.thumb" alt="comic.series">
                        <h4>{{comic.series}}</h4>
                    </div>
                    <div class="main__series__comics__btn">
                        <button>load more</button>
                    </div>
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
                comics: [
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                        "price": "$19.99",
                        "series": "Action Comics",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                        "price": "$3.99",
                        "series": "American Vampire 1976",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                        "price": "$16.99",
                        "series": "Aquaman",
                        "type": "graphic novel"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                        "price": "$2.99",
                        "series": "Batgirl",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        "price": "$3.99",
                        "series": "Batman",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        "price": "$2.99",
                        "series": "Batman Beyond",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                        "price": "$3.99",
                        "series": "Batman/Superman",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                        "price": "$4.99",
                        "series": "Batman/Superman Annual",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                        "price": "$5.99",
                        "series": "Batman: The Joker War Zone",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                        "price": "$6.99",
                        "series": "Batman: Three Jokers",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                        "price": "$4.99",
                        "series": "Batman: White Knight Presents: Harley Quinn",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                        "price": "$16.99",
                        "series": "Catwoman",
                        "type": "graphic novel"
                    }
                ],
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
    .main__jumbotron {
        background-image: url("../assets/img/jumbotron.jpg");
        background-position: top;
        background-size: cover;
        height: 400px;
    }
    .main__series {
        background-color: #1c1c1c;
        &__note {
            background-color: #0282f9;
            position: absolute;
            top: -30px;
            h3 {
                padding: 15px 20px;
                color: #fff;
                text-transform: uppercase;
            }
        }
        &__comics {
            padding: 50px 20px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            h3 {
                text-align: center;
                line-height: 172px;
                color: #fff;
            }
            &__container {
                width: calc(100%/6);
                margin-bottom: 30px;
                h4 {
                    margin: 10px 0;
                    color: #fff;
                    text-transform: uppercase;
                }
            }
            &__btn {
                button {
                    background-color: #0282f9;
                    text-transform: uppercase;
                    padding: 15px 40px;
                    font-weight: 700;
                    color: #fff;
                    border: none;
                }
            }
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
                    width: 70px;
                    height: 70px;
                    object-fit: contain;
                    margin-right: 10px;
                }
            }
        }
    }
</style>