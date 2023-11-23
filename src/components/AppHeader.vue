<script>
    export default {
        data() {
            return {
                navLinks: [
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
                        text: "collectibles",
                    },
                    {
                        text: "videos",
                    },
                    {
                        text: "fans",
                    },
                    {
                        text: "news",
                    },
                    {
                        text: "shop",
                    },

                ]
            };
        },
        methods: {},
    };
</script>

<template>
    <nav class="flex centered">
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="logo">
        </div>
        <ul class="flex">
            <li v-for="item in navLinks" :key="item.text"> 
                <a href="">
                    {{ item.text.toUpperCase() }}
                </a>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as *;
@use '../style/partials/variables' as *;

nav {
    background-color: white;
    height: 100px;
    &.flex {
        @include flex(row, space-between, center);
        .logo img {
            height: 70px;
        }
        ul {
            list-style: none;
            gap: .5rem;
            @include flex(row, space-around, center);
            align-content: center;
            height: 100%;
            li {
                height: 100%;
                @include flex(column, center, center);
                align-items: center;
                cursor: pointer;
                &:hover {
                    border-bottom: 4px solid $primary-blue;
                    a {
                        color: $primary-blue;
                    }
                }
                a {
                    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
                    font-size: small;
                    text-decoration: none;
                    color: black;
                }
                
            }
            
        }
    }
}
</style>
