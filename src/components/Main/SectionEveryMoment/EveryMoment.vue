<template>
    <div class="box">

        <div class="row row-cols-2">
            <div class="col-8">
                <div class="box-text" id="mission">
                    <h2 @click="getCounter()">EVERY MOMENT COUNTS</h2>
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
                            <li v-for="(info) in infoData" :key="info.id">
                                <i class="m-2" :class="(info.icon)"></i>
                                <span>{{formtNumber(info.cunter)}}</span>
                                <p>{{info.text}}</p>
                            </li>
                        </ul>

                </div>

            </div>

        </div>

    </div>

  
</template>

<script>

import ButtonGold from '../../common/ButtonGold.vue'
export default {
    components:{
        ButtonGold,
    },
    data: function(){
        return{
            infoData: [
                {
                    id: 0,
                    number: 2032,
                    cunter: 0,
                    text: 'Volunteers worldwide',
                    icon: 'fa-regular fa-heart'

                },
                {
                    id: 1,
                    number: 132,
                    cunter: 0,
                    text: 'Active projects',
                    icon: 'fa-solid fa-globe'

                },
                {
                    id: 2,
                    number: 3800000,
                    cunter: 0,
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
    },
    methods: {

        getCounter: function(){

            setTimeout(() => {

                this.infoData.forEach(element => {
    
                    let interval = 0
    
                    if(element.number > 1000 && element.number < 10000) {
    
                        interval = null
    
                        setInterval(() => {
                        if (element.number > element.cunter) {
                        element.cunter++
                        }
                        }, interval)
    
                    } else if (element.number > 100 && element.number < 999) {
    
                        interval = 50
    
                        setInterval(() => {
                        if (element.number > element.cunter) {
                        element.cunter++
                        }
                        }, interval)
                    
                    } else if (element.number > 100000){
                        
                        interval = 8
    
                        setInterval(() => {
                        if (element.number > element.cunter) {
                        element.cunter = element.cunter + 3000
                        console.log(element.cunter)
                        }
    
                        }, interval)
    
                        
                    }
    
                    clearInterval()
                    
                    
                });
            }, 2000)

     
        },

        formtNumber(item){
            if (item > 10000 && item < 1000000) {
                return (item / 10000).toFixed(1) + 'K'
            } else if (item > 1000000) {
                return (item / 1000000).toFixed(1) + 'M'
            }else {
                return item
            }
        }
    },
    created(){
        window.addEventListener('scroll', this.getCounter);

    },
    destroyed(){
        window.removeEventListener('scroll', this.getCounter);
    }

}
</script>

<style lang="scss" scoped>

@import '@/style/variables.scss'; 

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
        background-image: url('@/assets/charity/images/home-content-bg-1.jpg');
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