<template>
    <nav id="navbar">
        <!-- Avada Health Logo -->
        <img src="../../assets/img/medical_logo_2x_light.png" alt="Avada Health Logo">

        <!-- Links List -->
        <ul>
            <li v-for="(link, index) in sitePages"><a :href="link.link">{{ link.text }}</a></li>
            <li><button><a href="#">Make Appointment</a></button></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',

    props: {
        sitePages: Array,
        departments: Array
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/mixins' as *;
    
    nav#navbar {
        @include flex(row, space-between, center, no-wrap);
        padding: 3rem 4rem;

        img {
            width: 300px;

        }

        ul {
            @include flex(row, space-between, center, no-wrap);
            list-style-type: none;

            li {
                margin: 0 1rem;
            }
        }
    }
</style>