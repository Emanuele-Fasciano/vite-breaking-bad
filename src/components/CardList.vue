<script>
import MainCard from "./MainCard.vue"
import { store } from "../data/store.js"

export default {
    data() {
        return {
            store,
        }
    },

    components: {
        MainCard
    }
}
</script>

<template>
   <div class="container mt-4">
       <div class="found-cards py-3 ps-2">
           found cards 39
       </div>
        <div class="row row-cols-3 row-cols-lg-5">
                <MainCard 
                    v-for="card in store.cardsArray"
                    :name="card.name"
                    :type="card.archetype"
                    :img="card.card_images[0].image_url"/>
        </div>
   </div>
</template>

<style lang="scss" scoped>
 .container{
    background-color: white;

    .found-cards{
        background-color:rgb(19, 18, 18);
        color: white;
        font-weight: bold;
    }
 }
</style>
