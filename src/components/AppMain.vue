<template>
    <main>

        <Welcome />
        <Doctors />
        <Services />
    </main>
</template>

<script>
import Welcome from './AppMain Components/Welcome.vue'
import Doctors from './AppMain Components/Doctors.vue'
import Services from './AppMain Components/Services.vue'
export default {
    name: 'AppMain',

    components: {
        Welcome,
        Doctors,
        Services
    }
}
</script>

<style lang="scss" scoped>
    
</style>