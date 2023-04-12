<script>

export default{
    data(){
        return{

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
            <img src="../assets/svg-.svg" alt="">
        </div>

    </section>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

section{
    background-color: $back-6;
    padding: 5rem 0
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



</style>