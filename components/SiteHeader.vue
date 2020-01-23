<template>
    <div class="header">
        <div class="logo">
            <h1>Good Monday</h1>
        </div>
        <div class="links">
            <nuxt-link to="/">Home</nuxt-link>
            <nuxt-link to="/about/">About</nuxt-link>
        </div>
        <div class="login">
            <button> Login </button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "SiteHeader"
    }
</script>

<style scoped lang="scss">
    .header {
        display: flex;
        justify-content: space-around;
        padding: 20px;
        background-color: cadetblue;
    }
</style>