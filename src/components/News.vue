<script>

export default{
    data(){
        return{
            
        }
    },
    props:{
        image:String,
        text:String
    },
    methods:{
        getImagePath: function(img){
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}

</script>

<template>

    <div class="image-wrap">
        <img :src="getImagePath(image)">
        <h4>{{ text }}</h4>
        <p>By Emily Fields</p>
        <div class="date">
            <div class="day">07</div>
            <div class="month">MAY '19</div>
        </div>
    </div>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

.image-wrap{
    position: relative;

    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    h4{
        padding: 1rem 0;
        font-weight: 400;
    }

    p{
        font-family: 'Dancing Script', cursive;
        font-size: 10px;
    }
    .date{
        position: absolute;
        top: -20px;
        left: 20px;
        text-align: center;
        width: 70px;
        height: 200px;

        .day{
            background-color: $back-8;
            font-size: 1.5rem;
            font-family: 'Dancing Script', cursive;
            font-weight: bolder;
        }

        .month{
            font-size: 12px;
            font-weight: bold;
            background-color: $back-9;
            padding: 1rem 0;
        }
    }
}

</style>