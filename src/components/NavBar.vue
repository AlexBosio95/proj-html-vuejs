<template>
    <nav >
        <ul class="d-flex align-items-center">
            <li v-for="(item, index) in navItems" :key="index">{{item.text}}</li>
        </ul>
    </nav>
  
</template>

<script>
import Home from './Home.vue';
import Mission from './Mission.vue';
import Causes from './Causes.vue';
import Journal from './Journal.vue';



export default {
    components:{
        Home,
        Mission,
        Causes,
        Journal,
    },
    data: function(){
        return{
            navItems: [
                {
                    text: 'Home',
                    isClick: false,
                    link: '',
                },
                {
                    text: 'Mission',
                    isClick: false,
                    link: '',
                },
                {
                    text: 'Causes',
                    isClick: false,
                    link: '',
                },
                {
                    text: 'Journal',
                    isClick: false,
                    link: '',
                },
            ]

        }
    }

}
</script>

<style lang="scss" scoped>
    ul{
        list-style: none;
        height: 3rem;
        margin: 1rem 0rem;

        li{
            color: white;
            display: inline;
            margin: 0rem 2rem;
            text-transform: uppercase;
        }

        .active{
            
        }
    }



</style>