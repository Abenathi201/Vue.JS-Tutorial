<template>
    <router-link :to="{name: 'tutorial', params: {id: tutorial.id}}" class="card">
        <img :src="tutorial.image_url" :alt="tutorial.title">
        <div class="info">
            <h3> {{ tutorial.title }} </h3>
            <p> Description: {{ tutorial.desc }}</p>
            <p> Price: R {{ tutorial.price }}</p>
        </div>
    </router-link>
</template>

<script>

export default{
    props: ["tutorial"]
}
</script>

<style scoped>
    .card{
        margin: auto;
        margin-block: 70px;
        height: 400px;
        width: 400px;
    }

    .card img{
        width: 100%;
        height: 100%;
    }

    .info{
        
    }
</style>