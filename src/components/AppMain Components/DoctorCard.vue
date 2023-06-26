<template>
    <div class="doctor-card">

        <!-- Doctor card content (dynamically populated) -->
        <img :src="doctor.photo" alt="Doctor Photo">
        <div class="info">
            <h4>{{ doctor.name }}</h4>
            <span>{{ doctor.specialization }}</span>
            <p>{{ doctor.text }}</p>
            <a :href="doctor.facebookLink"><i class="fa-brands fa-facebook-f"></i></a>
            <a :href="doctor.twitterLink"><i class="fa-brands fa-twitter"></i></a>
            <a :href="doctor.instagramLink"><i class="fa-brands fa-instagram"></i></a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'DoctorCard',

    props: {
        doctor: Object
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;

    div.doctor-card {
        background-color: $white;
        width: calc(100% / 3);
        margin: 1.5rem;
        text-align: start;

        img {
            width: 100%;
        }

        div.info {
            padding: 2rem;

            h4 {
                text-transform: uppercase;
                font-weight: 400;
                margin-bottom: 1rem;
                font-size: 1.1rem;
            }

            span {
                margin-bottom: 1.5rem;
                display: inline-block;
            }

            p {
                margin-bottom: 1.5rem;
                line-height: 40px;
            }
        }
    }
</style>