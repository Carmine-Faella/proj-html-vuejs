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

      <div>
        <img src="../assets/logo-sidearea-1.png" alt="Logo Footer">
        <div>Let's get creative</div>
      </div>

      <div>
        <div><a href="#">maree.qode@gmail.com</a></div>
        <div>+44645 321 789</div>
      </div>

      <div>
        <div><a href="#">Avenue d'Auderghem 10</a></div>
        <div><a href="#">1040 Brussels, Brlgium</a></div>
      </div>

      <div>
        <div>Stay in touch with us</div>
        <div>
          <a href="#"><i class="fa-brands fa-twitter"></i></a>
          <a href="#"><i class="fa-brands fa-pinterest-p"></i></a>
          <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
        </div>
      </div>

    </div>
  </section>
  
</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;
@use '../styles/partial/variables.scss' as *;
@use '../styles/partial/-mixin.scss' as *;

section{
  background-color: $back-7;
}

.container{
  @include my-container;
  @include my-display-flex;
  justify-content: space-between;
  padding: 4rem 0;

  div{
    padding: 0.5rem 0;
    font-weight:300;

    a{
      text-decoration: none;
      color:$text-color-11;

      i{
        padding-right:1.5rem;
      }
    }
  }
}


</style>