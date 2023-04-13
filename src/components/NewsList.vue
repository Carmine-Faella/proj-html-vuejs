<script>

import News from './News.vue';

export default{
    components:{
        News
    },
    data(){
        return{
            newList:[
                {
                    url:'h-2-blog-img-1.jpg',
                    text:'This way, loves: a detailed guide through new design'
                },
                {
                    url:'h-2-blog-img-2.jpg',
                    text:'I try to give a people a different way of lookink art'
                },
                {
                    url:'h-2-blog-img-3.jpg',
                    text:'Introduce Richard Laperrière of those amazing features'
                },
            ]
        }
    }
}

</script>

<template>

    <section>
        <div class="box-cnt">

            <div v-for="news,index in newList" :key="index" class="box">

                <News
                :image="news.url"
                :text="news.text"
                />

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
    position: relative
}
.box-cnt{
    @include my-container;
    padding: 5rem 0;
}
.box{
    display: inline-block;
    margin: 10px;
    width: calc(100%/3 - 20px);
}
.arrow{
    position: absolute;
    display: inline-block;
    top: 10%;
    right: 0;
    margin-right: 10px;
    background-color: $back-8;
    width:30px;
    height: 30px;
    @include my-center
}

</style>