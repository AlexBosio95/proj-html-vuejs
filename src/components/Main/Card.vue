<template>

    <div class="ms_card">
        <i :class="(icon)"></i>
        <h5 class="mt-3">{{title}}</h5>
        <p>{{desc}}</p>
        <button>{{btnText}}</button>
        
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

@import '../../style/variables.scss'; 

    .ms_card{
        width: calc(100% / 4 - 0.6rem);
        margin: 0.3rem;
        text-align: center;
        color: $white;

            i{
                font-size: 3rem;
                color: $goldenrod;
            }

            p{
                font-size: 0.8rem;
                margin-top: 1.5rem;
                line-height: 1.5rem;
            }

            h5{
                font-size: 1rem;
            }

            button{
                border: none;
                background-color: $goldenrod;
                text-transform: uppercase;
                color: $white;
                padding: 0.3rem 1rem;
                margin-top: 0.5rem;
                font-size: 0.8rem;
            }

    }

</style>