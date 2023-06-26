<template>
    <div class="advantage-card">

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

    div.advantage-card {

        h3 {
            margin: 1rem auto;
            text-transform: uppercase;
            font-weight: 500;
            font-size: 1.4rem;
            width: 80%;
        }

        p {
            line-height: 40px;
        }
    }
</style>