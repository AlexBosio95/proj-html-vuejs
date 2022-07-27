<template>
  <main>

      <EveryMoment />
      <OurValues />
      <RecentCauses />
      <LatestArticles />

  </main>
</template>

<script>
import EveryMoment from './EveryMoment.vue';
import OurValues from './OurValues.vue';
import RecentCauses from './RecentCauses.vue';
import LatestArticles from './LatestArticles.vue';

export default {
    components:{
        EveryMoment,
        OurValues,
        RecentCauses,
        LatestArticles,
    }

}
</script>

<style lang="scss" scoped>

</style>