<template>
    <div class="container">
            <Title 
            :dataTitle="dataTitle"/>

            <div class="container-box">
                <BoxImage v-for="(image, index) in dataImage" :key="index"

                :urlImg = 'image.urlImg'
                :alt = 'image.alt'
                />

            </div>
    </div>
    
</template>

<script>
import Title from './Title.vue';
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
                    urlImg: '../assets/charity/images/avada-charity-fair-trade-featured-600x450.jpg',
                    alt: 'charity-fair'
                },
                {
                    urlImg: '../assets/charity/images/avada-charity-farming-featured-600x450.jpg',
                    alt: 'charity-farming'
                },
                {
                    urlImg: '../assets/charity/images/avada-charity-shelter-featured-600x450.jpg',
                    alt: 'charity-shelter'
                },
                {
                    urlImg: '../assets/charity/images/avada-charity-vaccines-featured-600x450.jpg',
                    alt: 'charity-vaccines'
                },
            ]

        }
    }
    

}
</script>

<style lang="scss" scoped>

@import '../style/variables.scss'; 

    .container-box{
        display: flex;
        justify-content: center;
    }

</style>