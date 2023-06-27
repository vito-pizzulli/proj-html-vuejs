<template>
    <div class="facility-card">

        <!-- Facility card content (dynamically populated) -->
        <h3>{{ facility.title }}</h3>
        <p>{{ facility.text }}</p>
    </div>
</template>

<script>
export default {
    name: 'FacilityCard',

    props: {
        facility: Object
    }
}
</script>

<style lang="scss" scoped>
    
</style>