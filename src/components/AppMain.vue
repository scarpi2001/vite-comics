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
    <main>
        <div class="container">
            <AppMainCardList />
        </div>
    </main>

</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

main {

    color: $tertiary;
    background-color: $secondary;
    padding: 50px 0;

    .container {
        display: flex;
        flex-wrap: wrap;
    }

}
</style>