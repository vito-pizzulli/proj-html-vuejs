<template>
    <div class="card">

        <!-- Advantage card content (dynamically populated) -->
        <img :src="advantage.icon" alt="Advantage Icon">
        <h3>{{ advantage.title }}</h3>
        <p>{{ advantage.text }}</p>
    </div>
</template>

<script>
export default {
    name: 'AdvantageCard',

    props: {
        advantage: Object
    }
}
</script>

<style lang="scss" scoped>
    
</style>