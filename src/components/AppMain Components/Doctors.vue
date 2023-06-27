<template>
    <div id="doctors">

        <!-- Upper title section -->
        <div class="title">
            <img src="../../assets/img/icon-5.png" alt="Doctors Icon">
            <h2>Meet Our Doctors</h2>
            <hr>
            <p>Sed Ut Perspiciatis Unde Omnis Iste Natus Error Sit Voluptatem Accusantium Doloremque Laudantium, Totam Rem Aperiam, Eaque Ipsa Quae Ab Illo Inventore Veritatis Et Quasi Architecto Beatae</p>
        </div>
        
        <!-- Bottom doctors list, populated by DoctorCard Components -->
        <div class="doctors-list">
            <DoctorCard v-for="doctor in doctors"
            :doctor="doctor"
        />
        </div>
    </div>
</template>

<script>
import DoctorCard from './DoctorCard.vue'
export default {
    name: 'Doctors',
    
    components: {
        DoctorCard
    },

    data() {
        return {
            doctors: [
                {
                    name: 'Jon Snow',
                    specialization: 'Anesthesiologist',
                    photo: './src/assets/img/doctor-1.jpg',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque',
                    facebookLink: '#',
                    twitterLink: '#',
                    instagramLink: '#'
                },
                {
                    name: 'Tony Stark',
                    specialization: 'Cardiologist',
                    photo: './src/assets/img/doctor-2.jpg',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque',
                    facebookLink: '#',
                    twitterLink: '#',
                    instagramLink: '#'
                },
                {
                    name: 'Anna Smith',
                    specialization: 'Nurse Practitioner',
                    photo: './src/assets/img/doctor-3.jpg',
                    text: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque',
                    facebookLink: '#',
                    twitterLink: '#',
                    instagramLink: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;

    div#doctors {
        background-color: #f5f5f5;
        text-align: center;
        padding: 7rem 0 5rem;

        div.title h2 {
            text-transform: uppercase;
        }

        div.doctors-list {
            @include flex(row, center, center, no-wrap);
            margin: 4rem auto;
            width: 70%;
        }
    }
</style>