<script>
export default {

}
</script>

<template>
    <div class="banner_container">
    </div>
</template>

<style scope lang="scss">
.banner_container {
    height: 300px;
    width: 100%;
    background-image: url('../assets/img/jumbotron.jpg');
    background-size: cover;
    animation: banner_movement 70s infinite;
}

@keyframes banner_movement {
    50% {
        background-position: center;
    }


    }</style>