<template>
    <div>
        <img :src="urlImg" :alt="alt">
    </div>
  
</template>

<script>
export default {
    props:{
        urlImg: String,
        alt: String,
    }

}
</script>

<style lang="scss" scoped>

@import '../style/variables.scss'; 

img{
    width: calc(100% / 4 - 1rem);
    margin: 0.5rem;
    height: 200px;
}

</style>