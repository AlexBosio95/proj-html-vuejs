<template>

    <header>
        <div class="container">
            <div class="row row-cols-2">
                <div class="col-5 logo-container" id="head">
                    <img src="@/assets/charity/images/avada-charity-logo.png" alt="">
                </div>
                <div class="col-7 d-flex justify-content-end">
                    <NavBar />
                </div>
            </div>
            <div class="text-container">
                <h1>MAKE A DIFFERENCE</h1>
                <div>
                    <span class="d-inline-block">As long as poverty, injustice & inequality persist, none of us can truly rest</span>
                </div>

                <div class="d-flex justify-content-center mt-5">
                    <ButtonBord v-for="(button, index) in dataButton" :key="index" 
                    :text = 'button.text'
                    :isCurrent = 'button.isCurrent'
                    />
                </div>
            </div>
        </div>
        
    </header>

</template>

<script>
import NavBar from './Header/NavBar.vue';
import ButtonBord from './common/ButtonBord.vue';


export default {
    components: {
        NavBar,
        ButtonBord,
    },

    data: function(){
        return{
            dataButton: [
                    {
                        text: 'our mission',
                        link: '#',
                        isClick: false,
                        isCurrent: false
                    },

                    {
                        text: 'donate now',
                        link: '#',
                        isClick: false,
                        isCurrent: true
                    }


                ]
        }
        
    }

}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 

header{
    background-image: url('@/assets/charity/images/home-page-slider.jpg');
    background-size: cover;
    background-position: center;
    height: 46rem;
    max-height: 46rem;
    background-attachment: fixed;

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

        
    }
}

</style>