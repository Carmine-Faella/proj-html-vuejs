<script>

export default{
    data(){
        return{

        }
    },
    props:{
        image:String,
        name:String
    },
    methods:{
        getImagePath: function(img){
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}

</script>

<template>

    <div class="card-cnt">
        <img :src="getImagePath(image)">
        <div class="hover">
            <h3>{{ name }}</h3>
            <div><i>Illustartion</i></div>
        </div>
    </div>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

.card-cnt{
    position: relative;

    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .hover{
        position: absolute;
        bottom: 50%;
        padding: 2rem 3rem;
        background-color: $back-primary;
        display: none;
    }
}

.card-cnt:hover .hover{
    display: block;
}

</style>