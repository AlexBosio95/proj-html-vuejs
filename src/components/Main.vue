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
import EveryMoment from './Main/EveryMoment.vue';
import OurValues from './Main/OurValues.vue';
import RecentCauses from './Main/RecentCauses.vue';
import LatestArticles from './Main/LatestArticles.vue';
import ChangeLife from './Main/ChangeLife.vue';

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