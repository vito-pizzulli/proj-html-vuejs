<template>
    <header>
        <Navbar
            :sitePages="sitePages"
            :departments="departments"
        />
    </header>
</template>

<script>
import Navbar from './AppHeader Components/Navbar.vue';
export default {
    name: 'AppHeader',

    components: {
        Navbar
    },
    
    props: {
        sitePages: Array,
        departments: Array
    }
}
</script>

<style lang="scss" scoped>
    
    header {
        background-image: url('../assets/img/header-image-homepage.jpg');
        background-size: 120%;
        background-position: top;
    }
</style>