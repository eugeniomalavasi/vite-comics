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

// MAIN STYLE
.main {
    background-color: $main-bck-color;
    padding: 5rem 2rem;
    h1 {
        color: white;
    }
}
</style>