<script>

import Card from './Card.vue';

export default{
    components:{
        Card
    },
    data(){
        return{
            cardList:[
                {
                    url:'h-2-port-img-1.jpg',
                    name:'Illustartion of Novels'
                },
                {
                    url:'h-2-port-img-2.jpg',
                    name:'Illustartion of Novels'
                },
                {
                    url:'h-2-port-img-3.jpg',
                    name:'Illustartion of Novels'
                },
                {
                    url:'h-2-port-img-4.jpg',
                    name:'Illustartion of Novels'
                },
                {
                    url:'h-2-port-img-5.jpg',
                    name:'Illustartion of Novels'
                },
                {
                    url:'h-2-port-img-6.jpg',
                    name:'Illustartion of Novels'
                }
            ]
        }
    }
}

</script>

<template>

    <div class="box-cnt">

        <div v-for="card,index in cardList" :key="index" class="box">

            <Card
            :image="card.url"
            :name="card.name"
            />

        </div>
        <div class="shop">
            <div class="interest"><img src="../assets/svg-4.svg"></div>
            <div class="bag-shop"><img src="../assets/svg-6.svg"></div>
            <div class="arrow"><img src="../assets/svg-2.svg"></div>
            <div class="arrow2"><img src="../assets/svg-2.svg"></div>
        </div>
    
    </div>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

.box-cnt{
    position: relative;

    .box{
        display: inline-block;
        width: calc(100%/3);
    }
}
.shop{
    img{
        width: 20px;
        height: 20px;
        display: block;
    }

    div{
        position: absolute;
        right: 0;
        width:30px;
        height: 30px;
        @include my-center
    }

    .interest{
        background-color: $back-11;
        top: 10%;
    }

    .bag-shop{
        background-color: $back-primary;
        top: 15%;
    }

    .arrow{
        top: 50%;
        background-color: $back-8;
        margin-right: 10px;
    }
    .arrow2{
        bottom: 20px;
        background-color: $back-8;
        margin-right: 10px;
    }
}



</style>