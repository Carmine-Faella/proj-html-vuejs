<script>

import Circle from './Circle.vue';

export default{
    components:{
        Circle
    },
    data(){
        return{
            circleItem:[
                {
                    icon:'fa-solid fa-lightbulb',
                    title:'First theres an idea',
                    color:'color-ligther'
                },
                {
                    icon:'fa-regular fa-comment',
                    title:'Then we talk about',
                    color:'color-message'
                },
                {
                    icon:'fa-solid fa-cloud',
                    title:'And we think about',
                    color:'color-cloud'
                },
                {
                    icon:'fa-solid fa-pen',
                    title:'So we draw along',
                    color:'color-pen'
                }
            ]
        }
    }
}

</script>

<template>

    <section>
        <h1 class="text-center">Working <span>process</span></h1>
        <div class="icon-cnt text-center">

            <div class="linear">
                <img src="../assets/svg-3.svg" alt="linear">
            </div>
            
            <div v-for="item,index in circleItem" :key="index">

                <Circle :title="item.title" :icon="item.icon" :color="item.color"/>

            </div>
        </div>
        <div class="arrow"><img src="../assets/svg-2.svg"></div>
    </section>

</template>


<style scoped lang="scss">

@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

section{
    position: relative;

    .icon-cnt{
    @include my-container;
    display: flex;
    position: relative;
    padding-bottom: 5rem;

    .linear{

        img{
        position: absolute;
        z-index: -1;
        width: 90%;
        padding-left: 5rem;
        }
    }
    
    }

    h1{
        padding: 3rem 0;
    }

    .text-center{
        text-align: center;
    }

    .arrow{
        position: absolute;
        display: inline-block;
        bottom: 10%;
        right: 0;
        margin-right: 10px;
        background-color: $back-8;
        width:30px;
        height: 30px;
        @include my-center
    }
}


</style>
