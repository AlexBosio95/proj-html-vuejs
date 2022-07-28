<template>
    <nav >
        <ul class="d-flex align-items-center">
            
            <li  v-for="(item, index) in navItems" :key="index" >
                <a :class="{'active' : (item.isClick)}" @click="getActive(index)" :href="`#${item.link}`">{{item.text}}</a>
            </li>
            <li>
                <ButtonGold 
                :dataButton = 'dataButton'/>
            </li>
        </ul>
    </nav>
  
</template>

<script>

import ButtonGold from '../common/ButtonGold.vue'

export default {

    components:{
        ButtonGold,
    },

    data: function(){
        return{
            navItems: [
                {
                    text: 'Home',
                    isClick: true,
                    link: '',
                },
                {
                    text: 'Mission',
                    isClick: false,
                    link: 'mission',
                },
                {
                    text: 'Causes',
                    isClick: false,
                    link: 'causes',
                },
                {
                    text: 'Journal',
                    isClick: false,
                    link: 'journal',
                },
            ],
            dataButton: 
                    {
                        text: 'donate',
                        link: '#',
                        isClick: false,
                        isCurrent: false
                    },
                

        }
    },
    methods: {

     getActive(current){
        this.navItems.forEach(element => {
            element.isClick = false
        });

        this.navItems[current].isClick = !this.navItems[current].isClick

    }    
    }

}
</script>

<style lang="scss" scoped>

@import '../../style/variables.scss'; 

    ul{
        list-style: none;
        height: 3rem;
        margin: 1rem 0rem;

        li{
            color: $white;
            display: inline;
            margin: 0rem 2rem;
            text-transform: uppercase;
            cursor: pointer;

            button{
                background-color: $goldenrod;
                color: $white;
                border: none;
                padding: 0.3rem 1rem;
                text-transform: uppercase;
            }

            a{
                color: $white;
                text-decoration: none;
            }
        }

    }

        .active{
            color: $goldenrod;
        }


</style>