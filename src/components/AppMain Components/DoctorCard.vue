<template>
    <div class="doctor-card">

        <!-- Doctor card content (dynamically populated) -->
        <img :src="doctor.photo" alt="Doctor Photo">
        <div class="info">
            <h4>{{ doctor.name }}</h4>
            <span>{{ doctor.specialization }}</span>
            <p>{{ doctor.text }}</p>
            <a :href="doctor.facebookLink" data-title="Facebook"><i class="fa-brands fa-facebook-f"></i></a>
            <a :href="doctor.twitterLink" data-title="Twitter"><i class="fa-brands fa-twitter"></i></a>
            <a :href="doctor.instagramLink" data-title="Instagram"><i class="fa-brands fa-instagram"></i></a>
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
        max-width: 350px;

        img {
            width: 100%;
            transition: all .3s;

            &:hover {
                transform: scale(1.05);
                box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
            }
        }

        div.info {
            padding: 2rem;

            h4 {
                text-transform: uppercase;
                font-weight: 400;
                margin-bottom: 1rem;
                font-size: 1.1rem;
                color: $charcoal;
            }

            span {
                margin-bottom: 1.5rem;
                display: inline-block;
                font-size: 1.1rem;
                color: $charcoal;
            }

            p {
                margin-bottom: 1.5rem;
                line-height: 40px;
                color: grey;
                width: 80%;
            }

            a {
                position: relative;

                &::after {
                    content: attr(data-title);
                    position: absolute;
                    bottom: 30px;
                    left: 50%;
                    transform: translateX(-50%);
                    background-color: $charcoal;
                    color: $lighter_grey;
                    padding: .3rem .5rem;
                    border-radius: 5px;
                    font-size: .8rem;
                    transition: all .3s;
                    opacity: 0;
                }

                &:hover::after {
                    opacity: 1;
                }
            }
        }
    }
</style>