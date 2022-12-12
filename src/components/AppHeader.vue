<script>

export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTER",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}

</script>


<template>
    <!-- HEADER -->
    <header>

        <!-- header nav -->
        <nav>
            <a href="#">
                <img src="img/dc-logo.png" alt="Dc Logo">
            </a>

            <!-- lista link -->
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a :class="{ active: link.current }" :href="link.url">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>

</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

header {

    height: 120px;

    nav {
        display: flex;
        justify-content: space-between;
        margin: 0 auto;
        max-width: 1200px;
        height: 100%;
        font-weight: 800;
        font-size: 12px;

        a {
            display: flex;
            align-items: center;

            img {
                width: 80px;
                height: 80px;
            }
        }
    }

}

ul {

    display: flex;
    align-items: center;
    list-style: none;

    li {
        margin: 0 15px;

        a {
            text-decoration: none;
            color: $secondary;
        }
    }

}
</style>