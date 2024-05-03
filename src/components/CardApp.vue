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
.card {
    img {
        max-width: 100%;
    }
}
</style>