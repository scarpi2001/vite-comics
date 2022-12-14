<script>
export default {
    name: "AppFooterMid",
    data() {
        return {
            menu: [
                {
                    title: "DC COMICS",
                    links: [
                        {
                            text: "Characters",
                            url: "#"
                        },
                        {
                            text: "Comics",
                            url: "#"
                        },
                        {
                            text: "Movies",
                            url: "#"
                        },
                        {
                            text: "TV",
                            url: "#"
                        },
                        {
                            text: "Games",
                            url: "#"
                        },
                        {
                            text: "Videos",
                            url: "#"
                        },
                        {
                            text: "News",
                            url: "#"
                        },
                    ]
                },
                {
                    title: "DC",
                    links: [
                        {
                            text: "Terms of use",
                            url: "#"
                        },
                        {
                            text: "Privacy",
                            url: "#"
                        },
                        {
                            text: "Ad Choices",
                            url: "#"
                        },
                        {
                            text: "Advertising",
                            url: "#"
                        },
                        {
                            text: "Jobs",
                            url: "#"
                        },
                        {
                            text: "Subscriptions",
                            url: "#"
                        },
                        {
                            text: "Talent",
                            url: "#"
                        },
                        {
                            text: "CPSC Certificates",
                            url: "#"
                        },
                        {
                            text: "Ratings",
                            url: "#"
                        },
                        {
                            text: "Shop Help",
                            url: "#"
                        },
                        {
                            text: "Contact Us",
                            url: "#"
                        },
                    ]
                },
                {
                    title: "SITES",
                    links: [
                        {
                            text: "DC",
                            url: "#"
                        },
                        {
                            text: "MAD Magazine",
                            url: "#"
                        }, {
                            text: "DC Kids",
                            url: "#"
                        }, {
                            text: "DC Universe",
                            url: "#"
                        }, {
                            text: "DC Power visa",
                            url: "#"
                        },
                    ]
                },
                {
                    title: "SHOP",
                    links: [
                        {
                            text: "Shop DC",
                            url: "#"
                        },
                        {
                            text: "Shop DC Collectibles",
                            url: "#"
                        },
                    ]
                },
            ]
        }
    }
}
</script>


<template>
    <!-- footer mid -->
    <section>

        <div class="container">

            <div id="mid_footer_menu">
                <!-- liste menu -->
                <div class="mid_footer_menu_list" v-for="(element, index) in menu" :key="index">
                    <h3>
                        {{ element.title }}
                    </h3>

                    <ul>
                        <li v-for="(link, index) in element.links" :key="index">
                            <a :href="link.url">
                                <span>
                                    {{ link.text }}
                                </span>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>

            <figure>
                <img src="../../../public/img/dc-logo-bg.png" alt="">
            </figure>

        </div>

    </section>
</template>

<style lang=scss scoped>
@use "../../styles/partials/variables" as*;


section {
    background-image: url(../../../public/img/footer-bg.jpg);
    height: 400px;
    background-size: cover;
    overflow: hidden;

    .container {
        display: flex;
        justify-content: space-between;

        #mid_footer_menu {
            display: flex;
            flex-wrap: wrap;
            padding: 30px 0;
            height: 250px;

            .mid_footer_menu_list {
                width: calc(100% / 3 - 20px);
                margin: 0 10px;

                h3 {
                    margin-bottom: 10px;
                }

                li {
                    list-style: none;
                }

                a {
                    color: #797979;
                    text-decoration: none;
                    font-size: 16px;

                    &:hover {
                        color: #fff;
                    }
                }
            }
        }

        figure {
            position: relative;
            bottom: 75px;
        }

    }
}
</style>