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
            <div class="text-container">
                <h1>MAKE A DIFFERENCE</h1>
                <div>
                    <span class="d-inline-block">As long as poverty, injustice & inequality persist, none of us can truly rest</span>
                </div>
                <button class="ms-btn">OUR MISSION</button>
                <button class="ms-btn donate">DONATE NOW</button>
            </div>
        </div>
        
    </header>

</template>

<script>
import NavBar from './Header/NavBar.vue';


export default {
    components: {
        NavBar,
    }

}
</script>

<style lang="scss" scoped>

@import '../style/variables.scss'; 

header{
    background-image: url('../assets/charity/images/home-page-slider.jpg');
    background-size: cover;
    background-position: center;
    height: 46rem;
    max-height: 46rem;

    .logo-container img{
        height: 3rem;
        margin: 1rem 0rem;
    }

    .text-container{
        color: $white;
        text-align: center;
        padding: 15.5rem 0rem;

        .ms-btn{
            border: 1px solid;
            color: $white;
            background-color: transparent;
            margin: 1.5rem 1rem;
            text-transform: uppercase;
            padding: 0.3rem 1.5rem;
        }

        h1{
            font-size: 3rem;
        }

        .donate{
            color: $goldenrod;
        }
    }
}

</style>