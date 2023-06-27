<template>
    <footer>
        <AboutUs
            :departments="departments"
        />
        <Copyright />
    </footer>
</template>

<script>
import AboutUs from './AppFooter Components/AboutUs.vue'
import Copyright from './AppFooter Components/Copyright.vue'
export default {
    name: 'AppFooter',

    components: {
        AboutUs,
        Copyright
    },

    props: {
        departments: Array
    }
}
</script>

<style lang="scss" scoped>
    
</style>