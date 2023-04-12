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
        </div>

    </section>

</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

.container{
    @include my-container;
}



</style>