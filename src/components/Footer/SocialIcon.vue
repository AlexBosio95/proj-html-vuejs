<template>
<div class="circle-icon">
    <a href=""><i :class="icon"></i></a>
    
</div>
  
</template>

<script>
export default {
    props:{
        icon: String,

    }

}
</script>

<style lang="scss" scoped>

@import '../../style/variables.scss'; 

.circle-icon{
    background-color: $white;
    width: 2.5rem;
    height: 2.5rem;
    border-radius: 50%;
    margin: 0.5rem;
    position: relative;

    i{
        font-size: 1.2rem;
        color: $goldenrod;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
}



</style>