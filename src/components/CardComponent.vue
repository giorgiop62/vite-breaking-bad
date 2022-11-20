<script>
import {store} from '../data/store'

export default {
  name:'CardComponent',
  data(){
    return{
      store
    }
  }

}

</script>

<template>
    <div class="sc-card col-4" v-for="attore in store.attoriLista" :key="attore.id">{{attore.name}}>
  
    </div>
    



  
</template>



<style lang="scss" scoped>
.sc-card{
  text-align: center;
  height: 100px;
  width: 200px;
  background-color: yellow;


}



</style>