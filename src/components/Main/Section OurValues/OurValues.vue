<template>
  <div class="our-values">

      <div class="container">

        <Title class="title"
        
          :dataTitle = 'dataTitle'
        />


      <div class="d-flex justify-content-center cards-container">

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
import Title from '../../common/Title.vue';

export default {
    components:{
        Card,
        Title,
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
                    icon: 'fa-solid fa-stethoscope',
                    title: 'Vaccinations',
                    desc: 'Nullam convallis, orci in congue aliquet, diam mauris cursus urna, Id maximus lectus magna maximus.',
                    btnText: 'Learn More'

                },
                {
                    icon: 'fa-solid fa-graduation-cap',
                    title: 'Education',
                    desc: 'Nullam convallis, orci in congue aliquet, diam mauris cursus urna, Id maximus lectus magna maximus.',
                    btnText: 'Learn More'

                },
                {
                    icon: 'fa-solid fa-wheat-awn',
                    title: 'Farming',
                    desc: 'Nullam convallis, orci in congue aliquet, diam mauris cursus urna, Id maximus lectus magna maximus.',
                    btnText: 'Learn More'

                },
                
            ],
            dataTitle: 
                {
                    title: 'OUR VALUES',
                    subtitle: 'Think Big. Act Bigger.'
                }
            
        }
    }

}
</script>

<style lang="scss">

@import '@/style/variables.scss'; 

    .our-values{
        background-image: url('@/assets/charity/images/home-content-bg-2.jpg');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        background-attachment: fixed;

        .cards-container{
            padding-top: 5rem;
            padding-bottom: 7rem;
        }


    }

    .title{
        color: $white;
    }

</style>