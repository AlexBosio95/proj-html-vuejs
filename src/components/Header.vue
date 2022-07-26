<template>

    <header>
        <div class="container">
            <div class="row row-cols-2">
                <div class="col logo-container">
                    <img src="../assets/charity/images/avada-charity-logo.png" alt="">
                </div>
                <div class="col">
                    <NavBar />
                </div>
            </div>
        </div>
        
    </header>

</template>

<script>
import NavBar from './NavBar.vue';


export default {
    components: {
        NavBar,
    }

}
</script>

<style lang="scss" scoped>

header{
    background-image: url('../assets/charity/images/home-page-slider.jpg');
    background-size: cover;

    .logo-container img{
        height: 3rem;
        margin: 1rem 0rem;
    }
}

</style>