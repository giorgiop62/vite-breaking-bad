<script>
import CardComponent from './CardComponent.vue'
import {store} from '../data/store'

export default {
  name:'AppMain',
  components: {
    CardComponent
  },

  data(){
    return{
      store

    }
  }

}
</script>


<template>
  <header>
      <div class="logo">
        <img src="/Breaking_Bad_logo.svg.png" alt="">
      </div>
      <h1>Breaking Bad Api</h1>
  </header>

  <select class="form-select">
      <option selected>Select Category</option>
      <option value="1">One</option>
      <option value="2">Two</option>
      <option value="3">Three</option>
    </select>

  <div class="container">

    <div class="input-group rounded">
    <input type="search" class="form-control rounded" placeholder="Founder" aria-label="Search" aria-describedby="search-addon" />
  </div>
  <div class="row">
    <CardComponent v-for="attore in store.attoriLista" :key="attore.id"
    :card="attore"/>

  </div>



    



  </div>

  

  
</template>



<style lang="scss" scoped>


select {
  width: 200px;
  margin-left: 300px;
  margin-bottom: 20px;
  
}

header {
  display: flex;
  align-items: center;
  height: 100px;


  img {
    width: 60px;
  }
  h1 {
    color: white;
    font-size: 40px;
  }
}


</style>