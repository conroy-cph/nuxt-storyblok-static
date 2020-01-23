<template>
    <div class="welcome">
        Welcome home!
        <nuxt-link class="nav__link" to="/about/">About</nuxt-link>
    </div>
</template>

<script>
import Test from "../components/test";

export default {
    components: {
        Test
    }
}
</script>

<style>
.welcome {
    color: hotpink;
}
</style>
