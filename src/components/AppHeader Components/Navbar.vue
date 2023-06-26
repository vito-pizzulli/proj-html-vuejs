<template>

    <nav id="header-navbar">

        <!-- Avada Health Logo -->
        <img src="../../assets/img/medical_logo_2x_light.png" alt="Avada Health Logo">

        <!-- Site pages List -->
        <ul>
            <li v-for="(link, index) in sitePages">
                <a :href="link.link">{{ link.text }}</a><span v-if="(index == 2)"><i class="fa-solid fa-angle-down"></i></span>
            </li>
            <li>
                <button><a href="#">Make Appointment</a></button>
            </li>
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
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;
    
    nav#header-navbar {
        @include flex(row, space-between, center, no-wrap);
        padding: 3rem 4rem;
        color: $white;

        img {
            width: 300px;
        }

        ul {
            @include flex(row, space-between, center, no-wrap);

            li {
                margin: 0 1.5rem;
                text-transform: uppercase;

                &:first-child a {
                    color: $teal;
                }

                span {
                    margin-left: .5rem;
                }

                button {
                    background-color: $teal;
                }
            }
        }
    }
</style>