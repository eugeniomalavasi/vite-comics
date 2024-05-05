<script>
export default {
    props: {
        thumb: String,
        price: String,
        series: String,
        type: String
    }
}
</script>

<template>
    <div class="card">
        <img :src="thumb" alt="">
        <p>{{ series }}</p>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/_mixins" as *;

.card {
    @include flex (column, center, center);

    &:hover p {
        color: $active-color;
    }

    &:hover img {
        filter: grayscale(100%);
        width: 500px;
        height: 110%;
        width: 180px;
        height: 180px;
    }

    img {
        max-width: 100%;
        // aspect-ratio: 1;
        width: 170px;
        height: 170px;
        object-fit: cover;

    }

    p {
        text-align: center;
        color: white;
        font-weight: 500;
        margin-top: 10px;
        font-size: 0.8rem;
        font-family: "Poller One", serif;
    }
}
</style>