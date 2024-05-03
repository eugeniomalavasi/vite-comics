<script>
export default {
    data() {
        return {
            siteMap: [
                {
                    title: "DC COMICS",
                    links: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "DC",
                    links: ["Terms of Use", "Privacy Policy (new)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talente Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"]
                },
                {
                    title: "SITES",
                    links: ["DC", "MAD Magazine", "DC kids", "DC Universe", "DC Power Visa"],
                },
                {
                    title: "SHOP",
                    links: ["Shop DC", "Shop DC Collectibles"]
                },
            ],
            icons: [
                {
                    name: "footer-facebook.png",
                },
                {
                    name: "footer-periscope.png",
                },
                {
                    name: "footer-pinterest.png",
                },
                {
                    name: "footer-twitter.png",
                },
                {
                    name: "footer-youtube.png",
                },
            ],
        }
    },
    methods: {
        getImageUrl(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        }
    },
}
</script>

<template>
    <div class="footer">
        <div class="container">
            <ul class="footer_list">
                <li v-for="(titles, index) in siteMap" class="foot_title">
                    {{ titles.title }}
                    <ul>
                        <li v-for="curLink in siteMap[index].links" class="foot_text">
                            <a href="">{{ curLink }}</a>
                        </li>
                    </ul>
                </li>
            </ul>
            <div class="logo_container">
            </div>
        </div>

        <!-- BOTTOM SOCIAL ICON FOOTER PART -->
        <div class="btm_foot_cont">
            <div class="bottom_footer">
                <a href="" class="sign">SIGN UP NOW!</a>
                <div>
                    <a href="" class="follow">FOLLOW US</a>
                    <ul>
                        <li v-for="img in icons">
                            <img :src="getImageUrl(img.name)" alt="social icon" class="social-icon">
                        </li>
                    </ul>
                </div>
            </div>
        </div>

    </div>
</template>

<style scoped lang="scss">
// IMPORT PARTIALS
@use "../style/partials/_mixins" as *;
@use "../style/partials/_variables" as *;

.container {
    @include flex (row, center, space-between);
    width: 80%;
    margin: 0 auto;

    .logo_container {
        height: 300px;
        width: 60%;
        background-image: url(../assets/img/dc-logo-bg.png);
        background-size: cover;
        background-position: center;
    }
}

.footer {
    background-image: url(../assets/img/footer-bg.jpg);

    .footer_list {
        @include flex(row, flex-start, flex-start);
        list-style-type: none;
        gap: 1.2rem;
        flex-wrap: wrap;

        .foot_title {
            font-size: 1rem;
            font-weight: 800;
            color: white;

            .foot_text {
                font-size: 0.8rem;
                color: $font-color;
                list-style-type: none;

                a {
                    color: $footer-text;
                    text-decoration: none;
                    font-weight: 400;

                    &:hover {
                        color: $active-color;
                    }
                }
            }
        }
    }

    .btm_foot_cont {
        background-color: #303030;

        .bottom_footer {
            width: 80%;
            margin: 0 auto;
            @include flex (row, center, space-between);
            height: 80px;

            ul {
                list-style-type: none;
                @include flex(row, center, center) 
            }
            .social-icon {
                padding: 5px;
            }
            .sign {
                color: white;
                text-decoration: none;
                border: 3px solid $active-color;
                padding: 1rem;
                border-radius: 5px;
                font-weight: 700;

                &:hover {
                    color: $active-color;
                }
            }

            .follow {
                text-decoration: none;
                font-weight: 700;
                color: $active-color;
            }

        }
    }

}
</style>