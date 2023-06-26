<template>
    <div class="info-card">
        <img :src="advantage.icon" alt="Advantage Icon">
        <h3>{{ advantage.title }}</h3>
        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptam accusantim</p>
    </div>
</template>

<script>
export default {
    name: 'InfoCard',

    props: {
        advantage: Object
    }
}
</script>

<style lang="scss" scoped>
    
</style>