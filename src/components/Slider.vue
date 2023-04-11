<script>

export default{
    data(){
        return{
            activeImage:0,
            sliderImg:[
                'h-2-slider-img-11.png',
                'h-2-slider-img-15.png',
                'h-2-slider-img-16.png'
            ]
        }
    },
    methods: {
        goToPrev(){
            this.activeImage--;
            if(this.activeImage < 0){
                this.activeImage = this.sliderImg.length - 1;
            }
        },
        goToNext(){
            this.activeImage++;
            if(this.activeImage == this.sliderImg.length){
                this.activeImage = 0;
            }
        },
        changeImage(index){
            this.activeImage = index
        }
    }
}

</script>

<template>
    <div class="container">

        <div>
            <div class="prevImg" @click="goToPrev"><i class="fa-solid fa-arrow-left"></i></div>
            <div class="nextImg" @click="goToNext"><i class="fa-solid fa-arrow-right"></i></div>
        </div>

        <div class="introdution">
            <h1>Devotion that never <i>ends</i></h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel, adipisci quisquam animi distinctio hic dicta dolore fugiat.</p>
        </div>
        <div class="img-wrap">
            <img :src="sliderImg[activeImage]">
        </div>

    </div>

    <div class="thumb-cnt">
        <div class="thumb" v-for="thumb,index in sliderImg" @click="changeImage(index)" :class="(activeImage==index)?'active':''"></div>
    </div>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
.container{
    margin: auto;
    max-width: 70%;
    display: flex;
    height: 500px;

    .introdution {
        width: 40%;
    }

    .img-wrap {
        width: 60%;
    }

    img{
        object-fit: contain;
        width: 100%;
        height: 100%;
    }

    h1{
        font-size: 4rem;
    }

    p{
        opacity: 0.5;
        padding: 2rem 0;
    }
}

.prevImg, .nextImg{
    width: 30px;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: $back-10;
    border-radius: 50%;
    position: absolute;  
    top: 50%;
    transform: translateY(-50%);
}

.prevImg{
    left: 50px;
}

.nextImg{
    right: 50px;
}

.thumb-cnt{
    display: flex;
    justify-content: center;
    padding: 2rem 0;

    .thumb{
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background-color: $back-10;
        margin: 0 0.5rem;
    }
}

.active{
    transform: scale(1.5);

}


</style>