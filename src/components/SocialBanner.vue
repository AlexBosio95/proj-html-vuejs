<template>
  <div class="bg-gray">
    <div class="container text-center py-3">
      <span class="opacity-50">© Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</span>
    </div>

    <div class="d-flex justify-content-center pb-4">

     <SocialIcon v-for="(social, index) in socialData" :key="index"
      :icon = 'social.icon'
      />
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

@import '../style/variables.scss'; 

  .bg-gray{
    background-color: $footer;

    span{
      text-transform: uppercase;
      font-size: 0.6rem;
      color: $gray-chateau;
    }
  }



</style>