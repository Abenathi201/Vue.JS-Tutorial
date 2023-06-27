<template>
    <div v-if="tutorials" class="flex-container">
        <Card v-for="tutorial of tutorials" :key="tutorial.id" :tutorial="tutorial" />
    </div>
    <div v-else>
        Loading...
    </div>
</template>

<script>
import Card from '@/components/Card.vue'

export default{
    components: { Card },

    computed: {
        tutorials() {
            return this.$store.state.tutorials
        }
    },

    mounted() {
        this.$store.dispatch("getTutorials")
    }
}
</script>

<style scoped>
    
    .flex-container{
        overflow: hidden;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        margin: auto;
    }
</style>