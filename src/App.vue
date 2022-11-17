
<script>
import axios from 'axios'
import AppMain from './components/AppMain.vue'


export default {
  name:'App',
  data(){
    return{
     
    }
  },
  components: {
    AppMain,
  },

  methods:{
    getActors(){
      axios.get(store.ApiUrl)
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
  <Actors />
  
</template>



<style lang="scss">
@use "./components/styles/genral.scss";


</style>