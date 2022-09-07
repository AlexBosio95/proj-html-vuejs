<template>
    <div>
        <button>{{gettextButton()}}</button>
    </div>
    
</template>

<script>
export default {
    props:{
        dataButton: Object,
        btnText: String,
    },
    methods:{
        gettextButton(){
            if (this.dataButton == '' || this.dataButton == null){
                return this.btnText
            } else {
                return this.dataButton.text
            }
        }
    }

}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 

    button{
        background-color: $goldenrod;
        border: none;
        color: $white;
        padding: 0.3rem 1.3rem;
        text-transform: uppercase;

        &:hover{
            background-color: $putty;
        }
    }

</style>