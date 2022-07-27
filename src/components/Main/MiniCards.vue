<template>
    <div class="d-flex horizontal-card">
        <div class="picture">
            <img :src="require(`../../assets/charity/images/${imgPath}`)" alt="">
        </div>

        <div class="description">
            <h6>{{title}}</h6>
            <p>{{text}}</p>
        </div>
        
    </div>
  
</template>

<script>

export default {
    props:{
        text: String,
        title: String,
        imgPath: String,
    }

}
</script>

<style lang="scss" scoped>

@import '../../style/variables.scss'; 

    .horizontal-card{
        height: 95px;
        
        
        .picture{
            width: 25%;

            img{
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }

        .description{
            width: 75%;
            padding-left: 1rem;

                h6{
                color: $goldenrod;
                }

                p{
                    font-size: 0.7rem;
                    line-height: 1.7rem;
                }
        }
    }



</style>