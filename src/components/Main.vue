<template>
  <main>

      <EveryMoment />
      <OurValues />
      <RecentCauses />
      <LatestArticles />
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
    }

}
</script>

<style lang="scss" scoped>

</style>