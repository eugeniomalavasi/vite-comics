<script>
export default {

}
</script>

<template>
    <div class="main">
        <h1>WEBSITE MAIN CONTENT</h1>
    </div>
</template>

<style scoped lang="scss">
// PARTIALS IMPORT
@use "../style/partials/_variables" as *;
@use "../style/partials/_mixins" as *;
// MAIN STYLE
.main {
    background-color: $main-bck-color;
    padding: 5rem 2rem;
    @include flex (row, center, center);

    h1 {
        color: white;
    }
}
</style>