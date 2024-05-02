<script>
export default {
    data() {
        return {
            siteMap: [
                {
                    title: "COMICS",
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
    <div>
        <h1>SONO IL FOOTER</h1>
        <div>
            <ul>
                <li v-for="titles in siteMap" class="foot_title">
                    {{ titles.title }}
                </li>
            </ul>
        </div>
    </div>
</template>
