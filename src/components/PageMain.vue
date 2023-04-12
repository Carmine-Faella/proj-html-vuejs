<script>

import Slider from './Slider.vue';
import CardList from './CardList.vue';
import CircleList from './CircleList.vue';
import SendMessage from './SendMessage.vue';
import NewsList from './NewsList.vue';

export default{
  components:{
    Slider,
    CardList,
    CircleList,
    SendMessage,
    NewsList
  },
  data(){
    return{

    }
  }

}

</script>

<template>
  <Slider/>
  <CardList/>
  <CircleList/>
  <SendMessage/>
  <NewsList/>
  
</template>

<style scoped lang="scss">
</style>