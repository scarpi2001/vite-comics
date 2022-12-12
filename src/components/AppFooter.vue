<script>
export default {
    name: "AppFooter",
    data() {
        return {
            links: [
                {
                    image: "img/buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS",
                    url: "#",
                },
                {
                    image: "img/buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url: "#",
                },
                {
                    image: "img/buy-comics-shop-locator.png",
                    text: "COMIC SHOP LOCATOR",
                    url: "#",
                },
                {
                    image: "img/buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url: "#",
                },
                {
                    image: "img/buy-dc-power-visa.svg",
                    text: "DC POWER VISA",
                    url: "#",
                },
            ]
        }
    }
}
</script>


<template>
    <!-- FOOTER -->
    <footer>

        <!-- footer nav -->
        <nav>

            <div class="container">

                <!-- lista links -->
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :href="link.url">
                            <img :src="link.image" :alt="link.text">
                            <span>
                                {{ link.text }}
                            </span>
                        </a>
                    </li>
                </ul>

            </div>

        </nav>

    </footer>

</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

footer {
    color: $tertiary;

    nav {
        background-color: $primary;

        .container {
            padding: 50px 0;
        }

        ul {
            display: flex;
            justify-content: space-between;
            align-items: center;
            list-style: none;

            li {
                margin: 0 15px;

                a {
                    display: flex;
                    align-items: center;
                    text-decoration: none;
                    color: $tertiary;

                    img {
                        width: 45px;
                        margin-right: 15px;
                    }
                }
            }
        }
    }
}
</style>