<template>
    <div class="d-flex horizontal-card">
        <div class="picture">
            <img :src="(urlToImage)" alt="">
        </div>

        <div class="description">
            <h6><a :href="url" target="_blank">{{getFormatString(title)}}</a></h6>
            <p>{{getFormatDescription(description)}}</p>
        </div>
        
    </div>
  
</template>

<script>

export default {
    props:{
        description: String,
        title: String,
        urlToImage: String,
        url: String,
    },

    data: function(){
        return{

        }
    },
    methods: {

        getFormatString(item){
            if (item != null) {

                if(item.length > 20){
                    return item.substr(0,65) + '...'
                }
            }

                
        },

        getFormatDescription(item){

            if (item != null) {

                if(item.length > 20){
                    return item.substr(0,145) + '...'
                }
            }

        },

    },

    created(){
        
    }

}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 

    .horizontal-card{
        height: 135px;
        margin: 0.4rem 0rem;
        
        
        .picture{
            width: 30%;

            img{
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }

        .description{
            width: 70%;
            padding-left: 1rem;

                a{
                color: $goldenrod;
                }

                p{
                    font-size: 0.7rem;
                    line-height: 1.7rem;
                }
        }
    }



</style>