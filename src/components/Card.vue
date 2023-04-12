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

    <div>
        <img :src="getImagePath(image)">
    </div>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;

img{
    width: 100%;
    height: 100%;
    object-fit: cover;
}

</style>