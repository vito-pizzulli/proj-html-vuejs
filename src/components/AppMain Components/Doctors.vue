<template>
    <div id="doctors">
        <img src="../../assets/img/icon-5.png" alt="Doctors Icon">
        <h2>Meet Our Doctors</h2>
        <hr>
        <p>Sed Ut Perspiciatis Unde Omnis Iste Natus Error Sit Voluptatem Accusantium Doloremque Laudantium, Totam Rem Aperiam, Eaque Ipsa Quae Ab Illo Inventore Veritatis Et Quasi Architecto Beatae</p>
        <DoctorCard v-for="doctor in doctors"
            :doctor="doctor"
        />
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
    
</style>