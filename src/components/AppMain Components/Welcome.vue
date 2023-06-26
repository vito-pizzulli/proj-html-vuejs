<template>
    <div id="welcome">
        <h1>Sono il componente Welcome</h1>
        <InfoCard />
    </div>
</template>

<script>
import InfoCard from '../Shared Components/InfoCard.vue'
export default {
    name: 'Welcome',

    components: {
        InfoCard
    },
}
</script>

<style lang="scss" scoped>
    
</style>