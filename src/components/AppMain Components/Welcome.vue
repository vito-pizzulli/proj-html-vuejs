<template>
    <div id="welcome">

        <!-- Upper title section -->
        <div class="title">
            <h2>Welcome To Avada Health</h2>
            <p>Sed Ut Perspiciatis Unde Omnis Iste Natus Error Sit Voluptatem Accusantium Doloremque Laudantium, Todam Rem Aperiam, Eaque Ipsa Quae Ab Illo</p>
        </div>

        <!-- Bottom advantages section, populated by AdvantageCard Components -->
        <div class="advantages">
            <AdvantageCard v-for="advantage in advantages"
                :advantage="advantage"
            />
        </div>
    </div>
</template>

<script>
import AdvantageCard from './AdvantageCard.vue'
export default {
    name: 'Welcome',

    components: {
        AdvantageCard
    },

    data() {
        return {
            advantages: [
                {
                    title: 'Same Day Appointments',
                    icon: './src/assets/img/icon-1.png',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptam accusantim'
                },
                {
                    title: 'World Class Facilities',
                    icon: './src/assets/img/icon-2.png',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptam accusantim'
                },
                {
                    title: 'Expert Doctors',
                    icon: './src/assets/img/icon-3.png',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptam accusantim'
                },
                {
                    title: 'Complementary Therapies',
                    icon: './src/assets/img/icon-4.png',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptam accusantim'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/mixins' as *;

    div#welcome {
        text-align: center;
        padding: 7rem 0 5rem;

        div.advantages {
            @include flex(row, center, center, no-wrap);
            width: 70%;
            margin: auto;
            padding: 3rem;
            text-align: center;
        }
    }
</style>