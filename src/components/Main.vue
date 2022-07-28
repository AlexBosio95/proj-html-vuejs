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
import EveryMoment from './Main/Section EveryMoment/EveryMoment.vue';
import OurValues from './Main/Section OurValues/OurValues.vue';
import RecentCauses from './Main/Section RecentCauses/RecentCauses.vue';
import LatestArticles from './Main/Section LastArticles/LatestArticles.vue';
import ChangeLife from './Main/Section ChangeLife/ChangeLife.vue';

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