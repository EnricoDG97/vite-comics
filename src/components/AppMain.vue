<script>
import AppBluebanner from './AppBluebanner.vue';
import AppJumbotron from './AppJumbotron.vue';
    export default {
    data() {
        return {};
    },
    methods: {},
    components: { AppBluebanner, AppJumbotron }
};
</script>

<template>


<AppJumbotron />

<section class="series-list centered">
<p>
    content goes here
</p>
</section>


<AppBluebanner />

</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.series-list.centered {
    @include flex(row, start, center);
    color: white;
    font-size: xx-large;
    // test
    background-color: $primary-darkgrey;
    height: 150px;
}


</style>
