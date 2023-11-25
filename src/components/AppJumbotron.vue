<script>
    export default {
        data() {
            return {

            };
        },
        methods: {},
    };
</script>

<template>
    <section>
        <img src="../assets/img/jumbotron.jpg" alt="jumbotron">
    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

section img  {
    display: block;
    height: 300px;
    width: 100%;
    object-fit: cover;
    object-position: top;
}

</style>