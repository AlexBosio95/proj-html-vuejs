<template>
    <div class="box">
        <img :src="require(`../../assets/charity/images/${pathImg}`)" :alt="alt">
    </div>
  
</template>

<script>
export default {
    props:{
        pathImg: String,
        alt: String
    },
    methods:{
        getpath(){
            console.log(this.pathImg)
        }
    }
    

}
</script>

<style lang="scss" scoped>

@import '../../style/variables.scss'; 

.box{
    width: calc(100% / 4 - 0.8rem);
    margin: 0.5rem;

    img{
    width: 100%;
}
}


</style>