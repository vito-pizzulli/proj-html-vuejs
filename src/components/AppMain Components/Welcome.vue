<template>
    <div id="welcome">
        <div class="title">
            <h2>Welcome To Avada Health</h2>
            <p>Sed Ut Perspiciatis Unde Omnis Iste Natus Error Sit Voluptatem Accusantium Doloremque Laudantium, Todam Rem Aperiam, Eaque Ipsa Quae Ab Illo</p>
        </div>
        <div class="advantages">
            <InfoCard v-for="advantage in advantages"
                :advantage="advantage"
            />
        </div>
    </div>
</template>

<script>
import InfoCard from '../Shared Components/InfoCard.vue'
export default {
    name: 'Welcome',

    components: {
        InfoCard
    },

    data() {
        return {
            advantages: [
                {
                    title: 'Same Day Appointments',
                    icon: './src/assets/img/icon-1.png'
                },
                {
                    title: 'World Class Facilities',
                    icon: './src/assets/img/icon-2.png'
                },
                {
                    title: 'Expert Doctors',
                    icon: './src/assets/img/icon-3.png'
                },
                {
                    title: 'Complementary Therapies',
                    icon: './src/assets/img/icon-4.png'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    
</style>