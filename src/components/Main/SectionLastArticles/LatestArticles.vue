<template>
    <div class="container" id="journal">
        <!-- Layout with Title and Description -->
        <Title 
        :dataTitle = 'dataTitle'
        />
        <div class="card-container">
        <div class="row ">
            <div class="col-12">
                    <BigCard 
                    :dataBigSlide = 'dataBigSlide'/>
                
            </div>

            <div v-if="!allArticles" class="col-12 d-flex flex-column g-4">
                <MiniCards v-for="(article, id) in articlesList" :key="id"
                    :description = 'article.description'
                    :title = 'article.title'
                    :urlToImage = 'article.urlToImage'
                    :url = 'article.url'
                />
            </div>

            <div v-if="allArticles" class="col-12 d-flex flex-column g-4">
                <MiniCards v-for="(article, id) in articlesListAll" :key="id"
                    :description = 'article.description'
                    :title = 'article.title'
                    :urlToImage = 'article.urlToImage'
                    :url = 'article.url'
                />
            </div>

        </div>

            <button @click="allArticles = !allArticles">view all our articles</button>

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

    props:{
        articlesList: Array,
        articlesListAll: Array,
    },
    
    data: function(){
        return{

            allArticles: false,

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
    },
    methods:{
        getArray(){
            // if (allArticles == true) {
            //     return articlesListAll
            // } else {
            //     return articlesList
            // }

            return articlesList
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