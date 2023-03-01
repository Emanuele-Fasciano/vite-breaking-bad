<script>
export default {
    data() {
        return {

        }
    },

    props: {
        name: String,
        type: String,
        img: String
    }
}
</script>

<template>
    <div class="col mb-3">
        <div class="mycard text-center">
            <img :src="img" alt="" class="img-fluid">
            <p class="text-white fw-bold">{{ name }}</p>
            <p class="type">{{ type }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables.scss" as *;
    .col{
        height: 400px;
        .mycard{
           height: 100%;
           position: relative;
           background-color: $primary-color;
           border: 1px solid black;

           .type{
            position: absolute;
            bottom: 0;
            margin-bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
           }
           }
    }
</style>
