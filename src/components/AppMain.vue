<script>
import AppMainCardList from "./main_components/AppMainCardList.vue"

export default {
    name: "AppMain",
    components: {
        AppMainCardList,
    }
}

</script>


<template>
    <!-- MAIN -->
    <section>
        <!-- container con labels e cards -->
        <div class="container">
            <span class="label">
                CURRENT SERIES
            </span>
            <AppMainCardList />
        </div>
    </section>

</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

section {
    color: $tertiary;
    background-color: $secondary;
    padding: 50px 0;

    .label {
        padding: 10px 30px;
        background-color: $primary;
        position: relative;
        bottom: 60px;
        font-size: 24px;
        font-weight: 800;
    }

}
</style>