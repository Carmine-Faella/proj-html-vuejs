<script>

export default{

    data(){
        return{
            
        }
    },
    props:{
        nav:Array
    }

}

</script>

<template>

    <div class="topbar">

        <div>
            <img src="../assets/logo-sidearea-1.png" alt="Logo header">
        </div>
        <nav>
            <li v-for="name in nav"><a :href="name.href">{{ name.name }}</a></li>
            <a href="#"></a><img src="../assets/svg-1.svg" alt="option">
        </nav>
       

    </div>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

.topbar{
    @include my-display-flex;
    justify-content: space-between;
    padding: 1rem;
    margin-bottom: 4rem;

    nav{
        @include my-display-flex;

        img{
            padding-left: 2rem;
            padding-right: 1rem;
        }
    }

    li{
        display: inline-block;
        padding: 0 1rem;
        list-style: none;

        &:hover{
            border-bottom: 4px solid $text-color-6;
        }

        a{
            text-decoration: none;
            color: $text-color-11;
        }
    }
}

</style>