<script>
    export default {
        data() {
            return {
                dccomics: [
                    {
                        text: "characters",
                    },
                    {
                        text: "comics",
                    },
                    {
                        text: "movies",
                    },
                    {
                        text: "tv",
                    },
                    {
                        text: "games",
                    },
                    {
                        text: "videos",
                    },
                    {
                        text: "news",
                    },
                ],
                shop: [
                    {
                        text: "shop dc",
                    },
                    {
                        text: "shop dc collectibles",
                    },
                ],
                dc: [
                    {
                        text: "terms of use",
                    },
                    {
                        text: "privacy policy (new)",
                    },
                    {
                        text: "ad choices",
                    },
                    {
                        text: "advertising",
                    },
                    {
                        text: "jobs",
                    },
                    {
                        text: "subscriptions",
                    },
                    {
                        text: "talent workshops",
                    },
                    {
                        text: "cpsc certificates",
                    },
                    {
                        text: "ratings",
                    },
                    {
                        text: "shop help",
                    },
                    {
                        text: "contact us",
                    },
                ],
                sites: [
                    {
                        text: "dc",
                    },
                    {
                        text: "mad magazine",
                    },
                    {
                        text: "dc kids",
                    },
                    {
                        text: "dc universe",
                    },
                    {
                        text: "dc power visa",
                    },
                ],
                socials: [
                    {
                        src: "footer-facebook.png",
                    },
                    {
                        src: "footer-twitter.png",
                    },
                    {
                        src: "footer-youtube.png",
                    },
                    {
                        src: "footer-pinterest.png",
                    },
                    {
                        src: "footer-periscope.png",
                    },
                ],
            };
        },
        methods: {
            getImageUrl(imgName) {
                return new URL(`../assets/img/${imgName}`, import.meta.url).href;
            }
        },
    };
</script>

<template>
        <section class="top-footer centered">
            <nav class="left-side">
                <div class="col-1">
                    <h2>dc comics</h2>
                    <ul>
                        <li v-for="link in dccomics" :key="link.text">
                            <a href="">{{ link.text }}</a>
                        </li>
                    </ul>
                    <h2>shop</h2>
                    <ul>
                        <li v-for="link in shop" :key="link.text">
                            <a href="">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-2">
                    <h2>dc</h2>
                    <ul>
                        <li v-for="link in dc" :key="link.text">
                            <a href="" target="_blank">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-3">
                    <h2>sites</h2>
                    <ul>
                        <li v-for="link in sites" :key="link.text">
                            <a href="">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
            <div class="right-side">
                <div class="logo-bg">
                    <img src="../assets/img/dc-logo-bg.png" alt="logo-bg">
                </div>
            </div>
        </section>

    <section class="bottom-footer centered">
        <div class="left-side">
            <button>sign up now!</button>
        </div>
        <div class="right-side">
            <h2>follow us:</h2>
            <ul class="icons">
                <li v-for="logo in socials" :key="logo.src" >
                    <img :src="getImageUrl(logo.src)" alt="logo">
                    <!-- <img src="../assets/img/footer-facebook.png" alt=""> -->
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.top-footer {
    background-image: url(../assets/img/footer-bg.jpg);
    @include flex(row, space-between, start);
    height: 300px;
    position: relative;
    .left-side {
        @include flex(row, space-between, start);
        padding: 20px 0;
        gap: 40px;
        .col-1 {
            @include flex(column, start, start)
        }
    }
    .right-side {
        height: 300px;
        width: 300px;
        position: relative;
        .logo-bg img {
            position: absolute;
            top: 50%;
            left: 20%;
            transform: translate(-50%, -50%);
            width: 150%;
            height: 150%;
            overflow: hidden;
        }
    }
}

ul {
    list-style-type: none;
    li {
        a {
            color: lighten($color: #303030, $amount: 40%);
            text-decoration: none;
            font-size: small;
            text-transform: capitalize;
            &:hover {
                cursor: pointer;
                color: white;
            }
        }
    }
}

h2 {
    margin-top: 6px;
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    text-transform: uppercase;
    text-decoration: solid;
    color: white;
    font-size: medium;
}
.bottom-footer {
    background-color: $primary-grey;
    @include flex(row, space-between, center);
    height: 100px;
    position: relative;
    z-index: 1;
    .left-side {
        button {
            padding: 8px 12px;
            border: 2px solid $primary-blue;
            background-color: transparent;
            text-transform: uppercase;
            color: white;
            &:hover {
                background-color: white;
                color: $primary-grey;
                cursor: pointer;
            }
        }
    }
    .right-side {
        @include flex(row, space-evenly, center);
        gap: 12px;
        h2 {
            color: $primary-blue;
            margin: 0;
        }
        .icons {
            @include flex(row, space-between, center);
            gap: 6px;
            img {
                height: 30px;
                width: 30px;
            }
        }
    }
}
</style>
