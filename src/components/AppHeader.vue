<script>

export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "character",
                    url: "#",
                    current: false,
                },
                {
                    text: "comics",
                    url: "#",
                    current: false,
                },
                {
                    text: "movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "games",
                    url: "#",
                    current: false,
                },
                {
                    text: "collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "news",
                    url: "#",
                    current: false,
                },
                {
                    text: "shop",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}

</script>

<template>

    <header>
        <nav>
            <a href="#">
                <img src="img/dc-logo.png" alt="Dc Logo">
            </a>

            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a class="active" href="#">
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

    height: 150px;

    nav {
        display: flex;
        justify-content: space-between;
        margin: 0 auto;
        max-width: 1000px;
        height: 100%;

        a {
            display: flex;
            align-items: center;
        }
    }

}

ul {

    display: flex;
    align-items: center;
    list-style: none;

    li {
        margin: 0 10px;

        a {
            text-decoration: none;
        }
    }

}
</style>