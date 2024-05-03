<script>
export default {
    data() {
        return {
            menuList: [
                {
                    text: "CHARACTER",
                    active: true
                },
                {
                    text: "COMICS",
                    active: false
                },
                {
                    text: "MOVIES",
                    active: false
                },
                {
                    text: "TV",
                    active: false
                },
                {
                    text: "GAMES",
                    active: false
                },
                {
                    text: "COLLECTIBLES",
                    active: false
                },
                {
                    text: "VIDEOS",
                    active: false
                },
                {
                    text: "FANS",
                    active: false
                },
                {
                    text: "NEWS",
                    active: false
                },
                {
                    text: "SHOP",
                    active: false
                },
            ],
            activeIndex: 0,
        }
    },
}
</script>

<template>
    <div class="header">
        <!-- LOGO -->
        <img src="../assets/img/dc-logo.png" alt="dc logo">
        <!-- MENU LIST -->
        <ul>
            <li v-for="(item, index) in menuList" :class="{ 'active': index === activeIndex }"
                @click="item.active = !item.active; activeIndex = index"><a href="">{{ item.text }}</a></li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
// IMPORT THE SCSS MIXINS 
@use "../style/partials/_mixins" as *;
@use "../style/partials/variables" as *;

.header {
    @include flex (row, center, space-between);
    width: 80%;
    margin: 0 auto;

    ul {
        @include flex (row, center, center);
        list-style-type: none;
        gap: 1rem;
        line-height: 150px;

        .active {
            border-bottom: 2px solid $active-color;
        }

        a {
            text-decoration: none;
            color: $font-color;
            font-weight: 800;

            &:hover {
                color: $active-color;
            }
        }
    }
}
</style>