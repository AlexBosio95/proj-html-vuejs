<template>
    <div class="bg-change-life">
        <div class="container">
            <Title class="title"
            :dataTitle = 'dataTitle'
            />

            <div class="d-flex justify-content-center mt-5">
                 <ButtonBord v-for="(button, index) in dataButton" :key="index"
                 :text = 'button.text'
                 />
            </div>

        </div>
    </div>
</template>

<script>
import Title from '../../common/Title.vue';
import ButtonBord from '../../common/ButtonBord.vue';

export default {
     components:{
        Title,
        ButtonBord,
    },

     data: function(){
        return{

            dataTitle: 
                {
                    title: 'change a life today',
                    subtitle: 'As long as poverty, injustice & inequality persist, none of us can truly rest. It doesn’t take much to change a life, Get in touch today and start making the difference.'
                },

                dataButton: [
                    {
                        text: 'volunteer',
                        link: '#',
                        isClick: false,
                        isCurrent: false
                    },

                    {
                        text: 'donate now',
                        link: '#',
                        isClick: false,
                        isCurrent: false
                    }


                ]
        }
     }
}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 

.bg-change-life{
    background-image: url('@/assets/charity/images/home-footer.jpg');
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    background-repeat: no-repeat;
    padding: 2rem 0 8rem 0;
}


</style>