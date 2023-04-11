<script>

import PageHeader from './components/PageHeader.vue';
import PageMain from './components/PageMain.vue';
import PageFooter from './components/PageFooter.vue';

export default{
  components:{
    PageHeader,
    PageMain,
    PageFooter
  },
  data(){
    return{
      navBar:[
                {
                    name:'Home',
                    href:'#home'
                },
                {
                    name:'Pages',
                    href:'#Pages'
                },
                {
                    name:'Portfolio',
                    href:'#Portfolio'
                },
                {
                    name:'Blog',
                    href:'#Blog'
                },
                {
                    name:'Shop',
                    href:'#Shop'
                },
                {
                    name:'Elements',
                    href:'#Elements'
                },
            ]
    }
  }
}

</script>

<template>

  <header>
    <PageHeader :nav="navBar"/>
  </header>

  <main>
    <PageMain/>
  </main>

  <footer>
    <PageFooter/>
  </footer>
  
</template>

<style lang="scss">
@use './styles/general.scss' as *;

</style>