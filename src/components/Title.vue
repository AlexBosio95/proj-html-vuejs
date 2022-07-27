<template>
    <div>
        <h3 class="text-center">{{dataTitle.title}}</h3>

            <div class="text-container d-flex justify-content-center">
                <div class="line-title"></div>
            </div>

        <span class="d-inline-block w-100 text-center">{{dataTitle.subtitle}}</span>
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

@import '../style/variables.scss'; 

        h3{
            padding-top: 5rem;
        }

        .line-title {
            width: 20%;
            background-color: $goldenrod;
            height: 0.2rem;
            margin-bottom: 2rem;
            margin-top: 1rem;
        }

        


</style>