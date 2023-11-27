<script>
    export default {
        props: {
            image: String,
            title: String,
        },
        data(){
            return {}
        },
        methods: {
            getImageUrl(imgName) {
                return new URL(imgName, import.meta.url).href;
            },
        },
    };
</script>

<template>
    <div class="card">
        <img :src="getImageUrl(image)" :alt="title" />
        <h2>
            {{ title }}
        </h2>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.card {
    img {
        width: 100%;
    }
    h2 {
        font-size: small;
        text-transform: uppercase;
        color: white;
    }
}

</style>