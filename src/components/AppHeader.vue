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
                    current: true,
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

        <section id="jumbotron"></section>
    </header>

</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

header {

    height: 400px;

    nav {
        display: flex;
        justify-content: space-between;
        margin: 0 auto;
        max-width: 1200px;
        height: 100px;
        font-weight: 600;
        font-size: 12px;

        a {
            display: flex;
            align-items: center;

            img {
                width: 80px;
                height: 80px;
            }
        }

        ul {
            display: flex;
            list-style: none;

            li {
                display: flex;
                align-items: center;
                margin: 0 15px;
                height: 100%;

                a {
                    height: 100%;
                    text-decoration: none;
                    color: $secondary;

                    &:hover {
                        color: $primary;
                        border-bottom: solid 3px $primary;
                    }
                }

            }

        }
    }

    #jumbotron {
        height: 300px;
        background-image: url(img/jumbotron.jpg);
        background-size: cover;
    }

    .active {
        color: $primary;
        border-bottom: solid 3px $primary;
    }
}
</style>