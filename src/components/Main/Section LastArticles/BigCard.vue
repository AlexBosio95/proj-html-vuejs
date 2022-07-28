<template>

    <div>
        <img :src="require(`@/assets/charity/images/${dataBigSlide.imgPath}`)" :alt="dataBigSlide.title">
        <div class="box-text">
            <h6>{{dataBigSlide.title}}</h6>
            <p>{{dataBigSlide.text}}</p>
        </div>
    </div>
  
</template>

<script>
export default {
    props:{
        dataBigSlide: Object
    }

}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 

 img{
        height: 18rem;
        width: 100%;
        object-fit: cover;
        border: 1px solid $footer;
    }

    .box-text{
        padding: 1rem;
        border: 1px solid $footer;

        
            h6{
                color: $goldenrod;
                margin: 1rem 0;
            }

            p{
                font-size: 0.7rem;
                line-height: 1.7rem;
            }
    }

</style>