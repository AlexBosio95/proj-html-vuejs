<template>
    <div>
        <button :class="{'donate' : (isCurrent)}">{{text}}</button>
    </div>
  
</template>

<script>
export default {
    props:{
        text: String,
        isCurrent: Boolean,
    }

}
</script>

<style lang="scss" scoped>

@import '../../style/variables.scss'; 

    button{
        background-color: transparent;
        border: 2px solid $white;
        color: $white;
        padding: 0.3rem 1.3rem;
        text-transform: uppercase;
        margin: 0 1.5rem;

        &:hover{
            background-color: $white;
            color: $goldenrod;
            border: 2px solid $goldenrod;
        }
    }

    .donate{
            color: $goldenrod;
            border: 2px solid $goldenrod;

        }

</style>