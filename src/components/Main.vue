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
import EveryMoment from './EveryMoment.vue';
import OurValues from './OurValues.vue';
import RecentCauses from './RecentCauses.vue';
import LatestArticles from './LatestArticles.vue';
import ChangeLife from './ChangeLife.vue';

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