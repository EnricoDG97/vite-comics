<script>
    export default {
        data() {
            return {
                shops: [
                    {
                        src: "buy-comics-digital-comics.png",
                        text: "digital comics",
                    },
                    {
                        src: "buy-comics-merchandise.png",
                        text:"dc merchandise",
                    },
                    {
                        src: "buy-comics-shop-locator.png",
                        text: "comic shop locator",
                    }, 
                    {
                        src: "buy-comics-subscriptions.png",
                        text: "subscriptions",
                    },
                    {
                        src: "buy-dc-power-visa.svg",
                        text: "dc power visa",
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
 <section class="blue-banner centered">
    <ul>
        <li class="col" v-for="shop in shops">
            <img :src="getImageUrl(shop.src)" alt="shop">
            <h5>{{ shop.text }}</h5>
        </li>
    </ul>
 </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.blue-banner.centered {
    background-color: $primary-blue;
    ul {
        @include flex(row, space-around, center);
        color: white;
        // test
        padding: 40px 0;
        .col {
            @include flex(row, center, center);
            gap: 10px;
            text-transform: uppercase;
            img {
                width: 40px;
            }
        }
    }
}
</style>