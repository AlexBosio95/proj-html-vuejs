<template>
    <nav >
        <ul class="d-flex align-items-center">
            <li :class="{'active' : (item.isClick)}" v-for="(item, index) in navItems" :key="index">{{item.text}}</li>
            <li>
                <button class="">donate</button>
            </li>
        </ul>
    </nav>
  
</template>

<script>

export default {

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

@import '../style/variables.scss'; 

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
        }

    }

        .active{
            color: $goldenrod;
        }


</style>