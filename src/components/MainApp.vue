<script>
import CardList from "./CardList.vue"

export default {
    data() {
        return {

        }
    },

    components: {
        CardList
    }
}
</script>

<template>
    <main>
        <CardList/>
    </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;

main{
    background-color: $primary-color;
    padding-top: 5rem;
}


</style>