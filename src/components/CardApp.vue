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
@use "../style/partials/_mixins" as *;

.card {
    @include flex (column, center, center);

    img {
        max-width: 100%;
        aspect-ratio: 1;
        object-fit: cover;
    }

    p {
        text-align: center;
        color: white;
        font-weight: 500;
        margin-top: 10px;
        font-size: 0.8rem;
    }
}
</style>