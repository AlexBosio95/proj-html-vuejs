<template>
  <div class="our-values">
      <div class="container">

        <h3 class="text-center">OUR VALUES</h3>
        <div class="text-container d-flex justify-content-center">
            <div class="line-title"></div>
        </div>
        <span class="d-inline-block w-100 text-center">Think Big. Act Bigger.</span>
      

      <div class="d-flex">

        <Card v-for="(card, index) in cardData" :key="index"

            :icon = 'card.icon'
            :title = 'card.title'
            :desc = 'card.desc'
            :btnText = 'card.btnText'
        />

      </div>

    </div>


      
  </div>
</template>

<script>
import Card from './Card.vue';

export default {
    components:{
        Card,
    },
    
    data: function(){
        return{
            cardData: [
                {
                    icon: 'fa-solid fa-droplet',
                    title: 'Clean Water',
                    desc: 'Nullam convallis, orci in congue aliquet, diam mauris cursus urna, Id maximus lectus magna maximus.',
                    btnText: 'Learn More'

                },
                {
                    icon: '',
                    title: 'Vaccinations',
                    desc: 'Nullam convallis, orci in congue aliquet, diam mauris cursus urna, Id maximus lectus magna maximus.',
                    btnText: 'Learn More'

                },
                {
                    icon: '',
                    title: 'Education',
                    desc: 'Nullam convallis, orci in congue aliquet, diam mauris cursus urna, Id maximus lectus magna maximus.',
                    btnText: 'Learn More'

                },
                {
                    icon: '',
                    title: 'Farming',
                    desc: 'Nullam convallis, orci in congue aliquet, diam mauris cursus urna, Id maximus lectus magna maximus.',
                    btnText: 'Learn More'

                },
                
            ]
        }
    }

}
</script>

<style lang="scss" scoped>

@import '../style/variables.scss'; 

    .our-values{
        background-image: url('../assets/charity/images/home-content-bg-2.jpg');
        background-size: cover;
        background-position: center;

        h3{
            color: $white;
            padding-top: 5rem;
        }

        .line-title {
            width: 20%;
            background-color: $goldenrod;
            height: 0.2rem;
            margin-bottom: 2rem;
            margin-top: 1rem;
        }

        span{
            color: $white;
        }

    }

</style>