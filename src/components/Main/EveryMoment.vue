<template>
    <div class="box">

        <div class="row row-cols-2">
            <div class="col-8">
                <div class="box-text">
                    <h2>EVERY MOMENT COUNTS</h2>
                    <div class="line"></div>
                    <p>Curabitur non mi et turpis pharetra vulputate. Cras consequat, risus nec commodo vehicula, nisi est laoreet leo, ac convallis nisi nibh id velit. Aliquam mattis metus a nisi pretium.</p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ac nibh vestibulum, laoreet ipsum quis, vestibulum nisi. Curabitur non mi et turpis pharetra vulputate. Ipsum dolor sit amet, consectetur adipiscing elit. Praesent ac nibh vestibulum, laoreet ipsum quis, vestibulum nisi.</p>
                    <p>Curabitur non mi et turpis pharetra vulputate. Cras consequat, risus nec commodo vehicula, nisi est laoreet leo, ac convallis nisi nibh id velit.</p>

                    <ButtonGold 
                        :dataButton = 'dataButton'/>
                    
                </div>
            </div>
            <div class="col-4">
                <div class="box-info d-flex align-items-center justify-content-center">
                        <ul>
                            <li v-for="(info, index) in infoData" :key="index">
                                <i class="m-2" :class="(info.icon)"></i>
                                <span>{{info.number}}</span>
                                <p>{{info.text}}</p>
                            </li>
                        </ul>

                </div>

            </div>

        </div>

    </div>

  
</template>

<script>

import ButtonGold from '../common/ButtonGold.vue'
export default {
    components:{
        ButtonGold,
    },
    data: function(){
        return{
            infoData: [
                {
                    number: 2032,
                    text: 'Volunteers worldwide',
                    icon: 'fa-regular fa-heart'

                },
                {
                    number: 132,
                    text: 'Active projects',
                    icon: 'fa-solid fa-globe'

                },
                {
                    number: 3.8 + 'M',
                    text: 'Donated',
                    icon: 'fa-solid fa-dollar-sign'

                },
            ],
            dataButton: 
                    {
                        text: 'our mission',
                        link: '#',
                        isClick: false,
                        isCurrent: false
                    },
        }
    }

}
</script>

<style lang="scss" scoped>

@import '../../style/variables.scss'; 

    .box-text{
        padding: 5rem;

        .line{
            width: 30%;
            background-color: $goldenrod;
            height: 0.2rem;
            margin-bottom: 1.5rem;
            margin-top: 1rem;
        }

        button{
            border: none;
            background-color: $goldenrod;
            color: $white;
            padding: 0.5rem 1rem;
        }
    }

    .box-info{
        height: 100%;
        background-image: url('../../assets/charity/images/home-content-bg-1.jpg');
        background-size: cover;
        background-position: center;
        text-align: center;
        color: $white;

        ul{
            list-style: none;

            i, span{
                font-size: 2.5rem;
            }
        }
    }

</style>