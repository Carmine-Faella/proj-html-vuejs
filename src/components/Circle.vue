<script>

export default{
    data(){
        return{

        }
    },
    props:{
        title:String,
        icon:String,
    }
}

</script>

<template>
    
        <div class="d-flex">
            <div class="icon"><i :class="icon"></i></div>
            <div class="circle-wrapper">
                <h3>{{ title }}</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            </div>
        </div>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;
.icon{
    width: 150px;
    height: 150px;
    border-radius: 50%;
    background-color: $back-6;
    @include my-display-flex;
    justify-content: center;

    i{
        font-size: 2rem;
    }

}

.d-flex{
    @include my-display-flex;
    flex-direction: column;
}

h3{
    padding: 2rem 0;
}

p{
    opacity: 0.5;
}
</style>