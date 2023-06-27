<template>
    <div id="facilities">

        <!-- Upper title section -->
        <div class="title">
            <img src="../../assets/img/icon-7.png" alt="Facilities Icon">
            <h2>Tour Our Facilities</h2>
            <hr>
            <p>Sed Ut Perspiciatis Unde Omnis Iste Natus Error Sit Voluptatem Accusantium Doloremque Laudantium, Totam Rem Aperiam, Eaque Ipsa Quae Ab Illo Inventore Veritatis Et Quasi Architecto Beatae</p>
            <img src="../../assets/img/play-icon.png" alt="Play Icon">
        </div>
        <FacilityCard />
    </div>
</template>

<script>
import FacilityCard from './FacilityCard.vue'
export default {
    name: 'Facilities',

    components: {
        FacilityCard
    },

    data() {
        return {
            facilities: [
                {
                    title: 'Emergency Care',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque',
                    link: '#'
                },
                {
                    title: 'Expert Diagnostics',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque',
                    link: '#'
                },
                {
                    title: 'Superb Rehabilitation',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque',
                    link: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/mixins' as *;
    @use '../../styles/partials/variables' as *;
    
    div#facilities {
        text-align: center;
        padding: 7rem 0 5rem;
        background-image: url('../../assets/img/paralax-bg-tour-facilities.jpg');
        color: white;

        div.title p {
            margin-bottom: 1.5rem;
        }
    }
</style>