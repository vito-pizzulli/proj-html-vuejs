<template>
    <div id="services">

        <!-- Upper title section -->
        <div class="title">
            <img src="../../assets/img/icon-6.png" alt="Services Icon">
            <h2>Our Health Services</h2>
            <hr>
            <p>Sed Ut Perspiciatis Unde Omnis Iste Natus Error Sit Voluptatem Accusantium Doloremque Laudantium, Totam Rem Aperiam, Eaque Ipsa Quae Ab Illo Inventore Veritatis Et Quasi Architecto Beatae</p>
        </div>

        <!-- Bottom services section, populated by ServiceCard Components -->
        <div class="services-list">
            <ServiceCard v-for="service in services"
                :service="service"
            />
        </div>
    </div>
</template>

<script>
import ServiceCard from './ServiceCard.vue'
export default {
    name: 'Services',

    components: {
        ServiceCard
    },

    data() {
        return {
            services: [
                {
                    title: 'Rehabilitation Center',
                    icon: './src/assets/img/icon-14.png',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas'
                },
                {
                    title: 'Dental Implants',
                    icon: './src/assets/img/icon-15.png',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas'
                },
                {
                    title: 'Medicine Research',
                    icon: './src/assets/img/icon-16.png',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas'
                },
                {
                    title: 'Blood Bank',
                    icon: './src/assets/img/icon-11.png',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas'
                },
                {
                    title: 'Pharmaceutical Advice',
                    icon: './src/assets/img/icon-12.png',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas'
                },
                {
                    title: 'Medical Counseling',
                    icon: './src/assets/img/icon-13.png',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/mixins' as *;

    div#services {
        text-align: center;
        padding: 7rem 0 5rem;

        div.title h2 {
            text-transform: uppercase;
        }
    }
</style>