
<script>
import axios from 'axios'
import AppMain from './components/AppMain.vue'
import CardComponent from './components/CardComponent.vue'
import {store} from './data/store'

export default {

  name:'App',
  data(){
    return{
      store,
      

      
     
    }
  },
  components: {
    AppMain,
    CardComponent
  },

  methods:{
     getActors(){
       axios.get(store.apiUrl)
     .then(result =>{
      store.attoriLista = result.data
     })
     .catch(error =>{
       console.log(error)
     })

   }

  },

  mounted(){
     this.getActors();
    

    
  }
  

}
</script>

<template>
  <AppMain />
  <CardComponent/>

</template>



<style lang="scss">
@use "./components/styles/genral.scss";


</style>