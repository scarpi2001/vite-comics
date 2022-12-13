<script>
export default {
    name: "AppFooterBottom",
    data() {
        return {
            links: [
                {
                    image: "img/footer-facebook.png",
                    text: "facebook",
                    url: "#",
                },
                {
                    image: "img/footer-periscope.png",
                    text: "periscope",
                    url: "#",
                },
                {
                    image: "img/footer-pinterest.png",
                    text: "pinterest",
                    url: "#",
                },
                {
                    image: "img/footer-twitter.png",
                    text: "twitter",
                    url: "#",
                },
                {
                    image: "img/footer-youtube.png",
                    text: "youtube",
                    url: "#",
                },
            ]
        }
    }
}
</script>


<template>
    <!-- footer bottom -->
    <section>
        <div class="container">
            <div id="button">
                <h3>SIGN-UP NOW!</h3>
            </div>

            <div class="socials">
                <h3>FOLLOW US</h3>
                <div class="socials_links">
                    <ul>
                        <li v-for="(link, index) in links" :key="index">
                            <a :href="link.url">
                                <img :src="link.image" :alt="link.text">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang=scss scoped>
@use "../../styles/partials/variables" as*;

section {
    background-color: #303030;
    padding: 20px 0;

    .container {
        display: flex;
        justify-content: space-between;

        #button {
            padding: 20px;
            border: 2px solid $primary;
        }

        .socials {
            display: flex;
            align-items: center;

            h3 {
                color: $primary;
                margin-right: 10px;
            }

            ul {
                display: flex;
                justify-content: space-between;
                align-items: center;
                list-style: none;

                li {
                    margin: 0 10px;
                }
            }
        }
    }
}
</style>