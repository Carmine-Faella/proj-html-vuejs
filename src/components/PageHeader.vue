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
        </nav>

    </div>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;

.topbar{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;

    li{
        display: inline-block;
        padding: 0 1rem;
        list-style: none;

        a{
            text-decoration: none;
            color: $text-color-11;
        }
    }
}

</style>