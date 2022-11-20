<script>
import {store} from '../data/store'

export default {
  name:'CardComponent',
  props:{
   card:Object
  },

  data(){
    return{
      store
    }
  }

}

</script>

<template>
  <!--name img stato serie  -->
  <div class="sc-card col-3">
    <img :src="card.img" alt="card.name">
    <h4>{{card.name}}</h4>
    <p>{{card.status}}</p>
    <p>{{card.category}}</p>


  

  </div>
  
    



  
</template>



<style lang="scss" scoped>
.sc-card{
  text-align: center;

  img{
    max-width: 100%;

  }
 
}



</style>