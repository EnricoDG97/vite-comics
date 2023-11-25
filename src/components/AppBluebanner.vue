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
 <section class="blue-banner centered">
    section 2
 </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

section.blue-banner.centered {
    @include flex(row, start, center);
    color: white;
    font-size: xx-large;
    // test
    background-color: $primary-blue;
    height: 150px;
}
</style>