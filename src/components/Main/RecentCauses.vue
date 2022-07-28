<template>
    <div>

        <div class="container" id="causes">
                <Title 
                :dataTitle="dataTitle"/>


                <div class="container-box">

                    <BoxImage v-for="(image, index) in dataImage" :key="index"

                    :pathImg = 'image.pathImg'
                    :alt = 'image.alt' 
                    />

                </div>

        </div>
                <button>VIEW ALL OUR CAUSES</button>

    </div>
    
</template>

<script>
import Title from '../common/Title.vue';
import BoxImage from './BoxImage.vue';

export default {
    components:{
        Title,
        BoxImage,
    },
    data: function(){
        return{

            dataTitle: 
                {
                    title: 'Recent Causes',
                    subtitle: 'We run projects in over 30 countries in 5 contintents'
                },

            dataImage: [
                {
                    pathImg: 'avada-charity-fair-trade-featured-600x450.jpg',
                    alt: 'charity-fair'
                },
                {
                    pathImg: 'avada-charity-farming-featured-600x450.jpg',
                    alt: 'charity-farming'
                },
                {
                    pathImg: 'avada-charity-shelter-featured-600x450.jpg',
                    alt: 'charity-shelter'
                },
                {
                    pathImg: 'avada-charity-vaccines-featured-600x450.jpg',
                    alt: 'charity-vaccines'
                },
            ]

        }
    }
    

}
</script>

<style lang="scss" scoped>

@import '../../style/variables.scss'; 

    .container-box{
        display: flex;
        justify-content: center;
        padding: 4rem 0rem;
    }

    button{
        width: 100%;
        border: none;
        padding: 3rem 0rem;
        background-color: $Burnt-sienna;
        color: $white;
    }

</style>