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
                },
                {
                    icon:'fa-regular fa-comment',
                    title:'Then we talk about',
                },
                {
                    icon:'fa-solid fa-cloud',
                    title:'And we think about',
                },
                {
                    icon:'fa-solid fa-pen',
                    title:'So we draw along',
                }
            ]
        }
    }
}

</script>

<template>

    <h1 class="text-center">Working process</h1>
    <div class="icon-cnt text-center">
        <img src="../assets/svg-3.svg" alt="linear">
        <div v-for="item,index in circleItem" :key="index">

            <Circle :title="item.title" :icon="item.icon"/>

        </div>
    </div>

</template>


<style scoped lang="scss">

@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;
.icon-cnt{
    @include my-container;
    display: flex;
    position: relative;

    img{
        position: absolute;
        z-index: -1;
        width: 90%;
        padding-left: 5rem;
    }
}

.text-center,h1{
    text-align: center;
    padding: 3rem 0;
}

</style>
