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
                    url:'h-2-blog-img-1.jpg',
                    name:'Illustartion of Novels'
                },
                {
                    url:'h-2-blog-img-2.jpg',
                    name:'Illustartion of Novels'
                },
                {
                    url:'h-2-blog-img-3.jpg',
                    name:'Illustartion of Novels'
                },
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

    <div v-for="card,index in cardList" :key="index">
        <Card
        :image="card.url"
        :name="card.name"
        />
    </div>

</template>

<style scoped lang="scss">

</style>