<script>

export default{

  data(){
    return{
      iconFoot:[
          'fa-brands fa-twitter',
          'fa-brands fa-pinterest-p',
          'fa-brands fa-facebook-f',
          'fa-brands fa-instagram'
      ],
      item1:[
        'maree.qode@gmail.com',
        '+44645 321 789'
      ],
      item2:[
        "Avenue d'Auderghem 10",
        '1040 Brussels, Brlgium'
      ],
      logo:[
        {
          url:'logo-sidearea-1.png',
          alt:'logo Footer',
          text:"Le's get creative"
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

      <div v-for="item in logo">
        <img :src="getImagePath(item.url)" :alt="item.alt">
        <div>{{ item.text }}</div>
      </div>

      <div>
        <div v-for="item in item1"><a href="#">{{ item }}</a></div>
      </div>

      <div>
        <div v-for="item in item2"><a href="#">{{item}}</a></div>
      </div>

      <div>
        <div>Stay in touch with us</div>
        <div>
          <a v-for="icon in iconFoot" href="#"><i :class="icon"></i></a>
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

