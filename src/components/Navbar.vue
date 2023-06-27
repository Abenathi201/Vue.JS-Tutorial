<template>
    <nav class="topNav">
        <router-link class="active" to="/">Home</router-link>
        <router-link to="/tutorials">Tutorial</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/Form">Form</router-link>
    </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
    .topNav{
        background: #333;
        overflow: hidden;
        width: 100vw;
    }
    
    router-link{
        float: left;
        color: #f2f2f2;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
    }
    .active{
        background: green;
    }
</style>