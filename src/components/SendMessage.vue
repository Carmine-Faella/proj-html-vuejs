<script>

export default{
    data(){
        return{
            imageBack:[
                {
                    url:'short-slider-rev-1-img-2.png',
                    cls:'img-flower'
                },
                {
                    url:'short-slider-rev-1-img-6.png',
                    cls:'img-flower2'
                },
                {
                    url:'short-slider-rev-1-img-1.png',
                    cls:'img-tree'
                },
                {
                    url:'short-slider-rev-1-img-4.png',
                    cls:'img-cloud'
                },
                {
                    url:'short-slider-rev-1-img-4.png',
                    cls:'img-cloud2'
                },
                {
                    url:'short-slider-rev-1-img-5.png',
                    cls:'img-cloud3'
                },
                {
                    url:'short-slider-rev-1-img-5.png',
                    cls:'img-cloud4'
                },
                {
                    url:'short-slider-rev-1-img-4.png',
                    cls:'img-cloud5'
                },
                {
                    url:'short-slider-rev-1-img-4.png',
                    cls:'img-cloud6'
                },
                {
                    url:'short-slider-rev-1-img-9.png',
                    cls:'img-tree2'
                }
            ]
        }
    },
    methods:{
        getImagePath: function(img){
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}

</script>

<template>

    <section>

        <div class="container">
            <h1>Want to work with us? Send us <span>a message!</span></h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Necessitatibus aut animi ipsa sit sunt, modi minus vero tenetur, veniam sint voluptates molestias beatae, dignissimos rem quisquam asperiores recusandae odit unde.</p>
            <button>CONTACT</button>
        </div>

        <div class="img-back">
            <img v-for='image in imageBack' :src="getImagePath(image.url)" alt="immagine sfondo" :class="image.cls">
        </div>

    </section>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

section{
    background-color: $back-6;
    padding: 5rem 0;
    position:relative
}
.container{
    @include my-container;
    text-align: center;

    button{
        padding: 1rem 3rem;
        background: none;
        border: none;
        background-color: $back-7;
        font-size: 12px;
        font-weight: bold;
        letter-spacing: 2px;

        &:hover{
            background-color: $back-8;
            transition: all 1s ease;
        }
    }

    p{
        padding: 3rem 0;
        opacity: 0.5;
    }
}

.img-back{
    img{
        position: absolute;
        filter: opacity(0.5);
    }

    .img-cloud{
        top: 0;
        transform: rotate(180deg);
        width: 200px;
        height: 80px;
        left: -50px;
    }

    .img-cloud3{
        top: 0;
        left: 200px;
        transform: rotate(180deg);
        width: 150px;
    }

    .img-cloud2{
        top: 0;
        transform: rotate(180deg);
        transform: rotateX(180deg);
        width: 200px;
        height: 80px;
        right: 0;
    }

    .img-cloud4{
        top: 0;
        right: 200px;
        transform: rotate(180deg);
        transform: rotateX(180deg);
        width: 150px;
    }

    .img-cloud5{
        bottom: 0;
        right: 15%;
        width: 250px;
        height: 70px;
    }

    .img-cloud6{
        bottom: 0;
        left: 20%;
        width: 100px;
        height: 40px;
        transform: rotatey(180deg);
    }

    .img-tree{
        right: 0;
        bottom: 0;
        width: 150px;
    }

    .img-tree2{
        left: 0;
        bottom: 0;
    }

    .img-flower{
        top: 100px;
        right: 150px;
    }

    .img-flower2{
        bottom: 20px;
        left: 200px;
    }
    
}


</style>