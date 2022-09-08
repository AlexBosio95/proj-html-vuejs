<template>
    <main>

        <EveryMoment />
        
        <OurValues />

        <RecentCauses />

        <LatestArticles 
        :articlesList = 'articlesList'
        :articlesListAll = 'articlesListAll'
        />

        <ChangeLife />

    </main>
</template>

<script>
import EveryMoment from './Main/SectionEveryMoment/EveryMoment.vue';
import OurValues from './Main/SectionOurValues/OurValues.vue';
import RecentCauses from './Main/SectionRecentCauses/RecentCauses.vue';
import LatestArticles from './Main/SectionLastArticles/LatestArticles.vue';
import ChangeLife from './Main/SectionChangeLife/ChangeLife.vue';

export default {
    components:{
        EveryMoment,
        OurValues,
        RecentCauses,
        LatestArticles,
        ChangeLife,
    },
    props:{
        articlesList: Array,
        articlesListAll: Array,
    }

}
</script>

<style lang="scss" scoped>

</style>