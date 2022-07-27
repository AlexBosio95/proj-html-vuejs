<template>
    <div>
        <button>{{text}}</button>
        
    </div>
  
</template>

<script>
export default {
    props:{
        text: String,
    }

}
</script>

<style lang="scss" scoped>

@import '../style/variables.scss'; 

    button{
        background-color: transparent;
        border: 2px solid $white;
        color: $white;
        padding: 0.5rem 1rem;
        text-transform: uppercase;
        margin: 0 1.5rem;
    }

</style>