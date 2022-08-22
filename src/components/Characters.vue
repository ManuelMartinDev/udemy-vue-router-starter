<template>
    <Character v-if="characters" v-for="character of characters" :image="character.image" :name="character.name"
        :status="character.status" :specie="character.species" :location="character.location"
        :gender="character.gender"></Character>

</template>

<script>

import Character from "@/components/Character.vue"

export default {
    components: {
        Character
    },
    data() {
        return {
            characters: null
        }
    },

    async created() {
        const response = await fetch("https://rickandmortyapi.com/api/character")
        const { results } = await response.json()
        this.characters = results


    }

}
</script>