<template>
    <div class="doctor-card">
        <img :src="doctor.photo" alt="Doctor Photo">
        <h4>{{ doctor.name }}</h4>
        <span>{{ doctor.specialization }}</span>
        <p>{{ doctor.text }}</p>
    </div>
</template>

<script>
export default {
    name: 'DoctorCard',

    props: {
        doctor: Object
    }
}
</script>

<style lang="scss" scoped>
    
</style>