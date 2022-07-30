<template>
  <div class="container" id="journal">
      <!-- Layout with Title and Description -->
      <Title 
      :dataTitle = 'dataTitle'
      />
      <div class="card-container">
        <div class="row row-cols-2 gx-4">
            <div class="col">
                    <BigCard 
                    :dataBigSlide = 'dataBigSlide'/>
                
            </div>

            <div class="col d-flex flex-column justify-content-between">

                <MiniCards v-for="(data, index) in dataSlide" :key="index"

                    :text= 'data.text'
                    :title= 'data.title'
                    :imgPath= 'data.imgPath'
                
                />

            </div>
        </div>

            <button>view all our articles</button>

      </div>
  </div>
</template>

<script>

import Title from '../../common/Title.vue';
import MiniCards from './MiniCards.vue';
import BigCard from './BigCard.vue';

export default {
     components:{
        Title,
        MiniCards,
        BigCard,
    },
    
    data: function(){
        return{

            dataTitle: 
                {
                    title: 'LATEST ARTICLES',
                    subtitle: 'Together we make all the difference'
                },

            dataSlide: [
                {
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Prasent ac nibh vestibulum, laoreet ipsum.',
                    title: 'The human story of uniqueness',
                    imgPath: 'photo-1444664597500-035db93e2323-177x142.jpg'
                },

                {
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Prasent ac nibh vestibulum, laoreet ipsum.',
                    title: 'Sustainable trade tactics',
                    imgPath: 'photo-1447430617419-95715602278e-177x142.jpg'
                },

                {
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Prasent ac nibh vestibulum, laoreet ipsum.',
                    title: 'Farmers making a difference',
                    imgPath: 'photo-1460230525622-630fe3294cd7-177x142.jpg'
                },

                {
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Prasent ac nibh vestibulum, laoreet ipsum.',
                    title: 'Meeting remote tribes in Peru',
                    imgPath: 'photo-1460600421604-5e138c208b9c-177x142.jpg'
                },

            ],

            dataBigSlide: 

                {
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Prasent ac nibh vestibulum, laoreet ipsum.',
                    title: 'Understanding community complexities',
                    imgPath: 'photo-1444213007800-cff19e1677ac.jpg'
                },

        
            
        }
    }

}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 
.card-container{
    padding: 5rem 13rem;

   

    button{
        width: 100%;
        border: none;
        padding: 0.5rem 0rem;
        background-color: $Burnt-sienna;
        color: $white;
        margin-top: 4rem;
        text-transform: uppercase;
    }
}

</style>