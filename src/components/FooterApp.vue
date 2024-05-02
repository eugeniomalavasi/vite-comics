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
                    links: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "SITES",
                    links: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "SHOP",
                    links: ["Shop DC", "Shop DC Collectibles"],
                },
                {
                    title: "DC",
                    links: ["Shop DC", "Shop DC Collectibles"],
                },
            ]
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
            <div>
                <img src="../assets/img/dc-logo-bg.png" alt="dc logo transparent" class="logo">
            </div>
        </div>

        <!-- BOTTOM SOCIAL ICON FOOTER PART -->
        <div class="btm_foot_cont">
            <div class="bottom_footer">
                <a href="" class="sign">SIGN UP NOW!</a>
                <div>
                    <a href="" class="follow">FOLLOW US</a>
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

}

.footer {
    background-image: url(../assets/img/footer-bg.jpg);
    height: 300px;

    .footer_list {
        @include flex(row, center, center);
        list-style-type: none;
        gap: 1rem;

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

    .logo {
        max-height: 300px;
    }

    .btm_foot_cont {
        background-color: #303030;

        .bottom_footer {
            width: 80%;
            margin: 0 auto;
            @include flex (row, center, space-between);
            height: 80px;

            .sign {
                color: white;
                text-decoration: none;
                border: 1px solid $active-color;
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