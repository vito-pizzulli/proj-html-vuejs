<template>
    <div class="facility-card">

        <!-- Facility card content (dynamically populated) -->
        <h3>{{ facility.title }}</h3>
        <img src="../../assets/img/wave-divider.png" alt="Wave Divider Image">
        <p>{{ facility.text }}</p>
        <button><a :href="facility.link">Learn more</a></button>
    </div>
</template>

<script>
export default {
    name: 'FacilityCard',

    props: {
        facility: Object
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;

    div.facility-card{
        width: calc(100% / 3);
        padding: 4rem 1rem;

        &:first-of-type {
            background-color: $teal;
        }

        &:nth-of-type(2) {
            background-color: $sky_blue;
        }

        &:nth-of-type(3) {
            background-color: $blue;
        }

        h3, img {
            margin-bottom: .7rem;
        }

        h3 {
            font-weight: 500;
            font-size: 1.4rem;
        }

        p {
            font-weight: 500;
            line-height: 40px;
            margin-bottom: 1rem;
        }

        button {
            background-color: transparent;
            color: $white;
            border: 2px solid $white;
            transition: all .2s;

            a {
                transition: all .2s;
            }

            &:hover {
                background-color: $white;

                a {
                    color: $teal;
                }
            }
        }
    }
</style>