<template>
  <div class="bg-gray position-relative">
    <div class="container text-center py-3">
      <span class="opacity-50">© Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</span>
    </div>

    <div class="d-flex justify-content-center pb-4">

     <SocialIcon v-for="(social, index) in socialData" :key="index"
      :icon = 'social.icon'
      />
    </div>
    <div class="arrow-up">
      <a href="#head"><i class="fa-solid fa-chevron-up mt-2"></i></a>
    </div>
  </div>
</template>

<script>
import SocialIcon from './SocialIcon.vue'
export default {
  components:{
    SocialIcon,
  },
  data: function(){
    return{
      socialData: [
        {
          icon: 'fa-brands fa-facebook-f',
          text: 'facebook'
        },
        {
          icon: 'fa-brands fa-instagram',
          text: 'instagram'
        },
        {
          icon: 'fa-brands fa-twitter',
          text: 'twitter'
        },
        {
          icon: 'fa-brands fa-youtube',
          text: 'youtube'
        },
      ]
    }

  }


}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 

  .bg-gray{
    background-color: $footer;

    span{
      text-transform: uppercase;
      font-size: 0.6rem;
      color: $gray-chateau;
    }

    .arrow-up{
      cursor: pointer;
      position: absolute;
      right: 2rem;
      bottom: 0;
      background-color: $tuna;
      height: 2rem;
      width: 3rem;
      text-align: center;
      border-radius: 0.2rem 0.2rem 0 0;

      a{
      color: $white;
      }
    }

    
  }



</style>