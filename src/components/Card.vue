<template>

    <div>
        <i :class="(icon)"></i>
        
    </div>

  
</template>

<script>
export default {

    props:{
        icon: String,
        title : String,
        desc : String,
        btnText : String,
    }

}
</script>

<style lang="scss" scoped>

@import '../style/variables.scss'; 

    i{
        font-size: 3rem;
        color: $goldenrod;
    }

</style>