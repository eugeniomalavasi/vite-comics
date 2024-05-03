<script>
export default {
    data() {
        return {
            iconArrary: [
                {
                    image: "buy-comics-digital-comics.png",
                    title: "DIGITAL COMICS",
                },
                {
                    image: "buy-comics-merchandise.png",
                    title: "DC MERCHANDISE",
                },
                {
                    image: "buy-comics-subscriptions.png",
                    title: "SUBSCRIPTION",
                },
                {
                    image: "buy-comics-shop-locator.png",
                    title: "COMIC SHOP LOCATOR",
                },
                {
                    image: "buy-dc-power-visa.svg",
                    title: "DC POWER VISA",
                },
            ]
        }
    }, methods: {
        getImageUrl(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        }
    },
}
</script>

<template>
    <div class="icon_container">
        <ul>
            <li v-for="icon in iconArrary">
                <img :src="getImageUrl(icon.image)" alt="">
                <p>{{ icon.title }}</p>
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
// IMPORT THE SCSS MIXINS 
@use "../style/partials/_mixins" as *;
@use "../style/partials/variables" as *;

.icon_container {
    background-color: $active-color;

    ul {
        @include flex (row, center, space-between);
        list-style: none;
        color: white;
        width: 80%;
        margin: 0 auto;

        li {
            @include flex (row, center, center);
            gap: 1rem;
            padding: 2rem;
            font-size: 0.8rem;
            font-weight: 700;
        }
    }

    img {
        height: 50px;
    }
}
</style>