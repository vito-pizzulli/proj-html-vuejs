<template>
    <div class="card">
        
        <!-- Service card content (dynamically populated) -->
        <img :src="service.icon" alt="Service Icon">
        <h3>{{ service.title }}</h3>
        <p>{{ service.text }}</p>
    </div>
</template>

<script>
export default {
    name: 'ServiceCard',

    props: {
        service: Object
    }
}
</script>

<style lang="scss" scoped>

    div.card {
        width: calc(100% / 3);
        margin-bottom: 5rem;

        p {
            width: 95%;
        }
    }
</style>