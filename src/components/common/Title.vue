<template>
    <div>
        <h3 class="text-center">{{dataTitle.title}}</h3>

            <div class="d-flex justify-content-center flex-column ">
                <div class="line-title align-self-center"></div>
                <div class="w-50 text-center align-self-center">
                    <span>{{dataTitle.subtitle}}</span>
                </div>
            </div>

            

    </div>

</template>

<script>
export default {
    props:{
        dataTitle: Object,
    }

}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 

        h3{
            padding-top: 5rem;
            text-transform: uppercase;
        }

        .line-title {
            width: 10%;
            background-color: $goldenrod;
            height: 0.2rem;
            margin-bottom: 2rem;
            margin-top: 1rem;
        }

        


</style>