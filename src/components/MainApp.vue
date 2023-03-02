<script>
import CardList from "./CardList.vue"

export default {
    data() {
        return {
            types: [
                "Effect Monster",
                "Flip Effect Monster",
                "Flip Tuner Effect Monster",
                "Gemini Monster",
                "Normal Monster",
                "Normal Tuner Monster",
                "Pendulum Effect Monster",
                "Pendulum Effect Ritual Monster",
                "Pendulum Flip Effect Monster",
                "Pendulum Normal Monster",
                "Pendulum Tuner Effect Monster",
                "Ritual Effect Monster",
                "Ritual Monster",
                "Spell Card",
                "Spirit Monster",
                "Toon Monster",
                "Trap Card",
                "Tuner Monster",
                "Union Effect Monster",
                "Fusion Monster",
                "Link Monster",
                "Pendulum Effect Fusion Monster",
                "Synchro Monster",
                "Synchro Pendulum Effect Monster",
                "Synchro Tuner Monster",
                "XYZ Monster",
                "XYZ Pendulum Effect Monster",
                "Skill Card",
                "Token"
            ]
        }
    },

    emits: [
        "search"
    ],

    components: {
        CardList
    }
}
</script>

<template>
    <main>
        <select class="form-select" aria-label="Default select example">
            <option :value=" type "
                    v-for=" type, in types"
                    > {{ type }} 
            </option>
            </select>
            <button @click="$emit('search', value)">
                aa
            </button>
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