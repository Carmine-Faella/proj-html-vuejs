<script>

import Slider from './Slider.vue';
import CardList from './CardList.vue';
import CircleList from './CircleList.vue';
import SendMessage from './SendMessage.vue';

export default{
  components:{
    Slider,
    CardList,
    CircleList,
    SendMessage
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
</template>

<style scoped lang="scss">
</style>