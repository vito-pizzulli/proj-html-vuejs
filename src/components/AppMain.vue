<template>
    <main>

        <Welcome />
        <Doctors />
    </main>
</template>

<script>
import Welcome from './AppMain Components/Welcome.vue'
import Doctors from './AppMain Components/Doctors.vue'
export default {
    name: 'AppMain',

    components: {
        Welcome,
        Doctors
    }
}
</script>

<style lang="scss" scoped>
    
</style>