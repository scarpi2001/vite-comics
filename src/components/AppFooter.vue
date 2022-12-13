<script>
import AppFooterNav from './footer_components/AppFooterNav.vue';
import AppFooterMid from './footer_components/AppFooterMid.vue';
import AppFooterBottom from './footer_components/AppFooterBottom.vue';

export default {
    name: "AppFooter",
    components: {
        AppFooterNav,
        AppFooterMid,
        AppFooterBottom,
    }
}
</script>


<template>
    <!-- FOOTER -->
    <footer>

        <AppFooterNav />
        <AppFooterMid />
        <AppFooterBottom />

    </footer>

</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

footer {
    color: $tertiary;
}
</style>