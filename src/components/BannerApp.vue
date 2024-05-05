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
    background-position: top;
    animation: banner_movement 80s infinite;
}

@keyframes banner_movement {
    50% {
        background-position: center;
    }


    }</style>