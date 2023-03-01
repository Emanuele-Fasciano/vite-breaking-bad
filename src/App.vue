<script>
  import AppHeader from "./components/AppHeader.vue"
  import MainApp from "./components/MainApp.vue"
  import axios from "axios"
  import { store } from "./data/store"

  export default {
    data(){
      return{
        
      }
    },
    
    components: {
    MainApp,
    AppHeader
},

    created(){
      axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0")
      .then((response)=>{
        store.cardsArray = response.data.data
      })

    }
  }
</script>

<template>
  <AppHeader/>
  <MainApp/>
</template>

<style lang="scss"> 
@use "./assets/scss/style.scss"
</style>

