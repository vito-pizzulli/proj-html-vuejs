<template>
    <main>

        <Welcome />
        <Doctors />
        <Services />
        <Facilities />
        <AppointmentForm />
    </main>
</template>

<script>
import Welcome from './AppMain Components/Welcome.vue'
import Doctors from './AppMain Components/Doctors.vue'
import Services from './AppMain Components/Services.vue'
import Facilities from './AppMain Components/Facilities.vue'
import AppointmentForm from './AppMain Components/AppointmentForm.vue'
export default {
    name: 'AppMain',

    components: {
        Welcome,
        Doctors,
        Services,
        Facilities,
        AppointmentForm
    }
}
</script>

<style lang="scss" scoped>
    
</style>