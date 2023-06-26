<template>
    <header>
        <h1>Sono l'Header</h1>
        <Navbar />
    </header>
</template>

<script>
import Navbar from './AppHeader Components/Navbar.vue';
export default {
    name: 'AppHeader',

    components: {
        Navbar
    }
}
</script>

<style lang="scss" scoped>
    
</style>