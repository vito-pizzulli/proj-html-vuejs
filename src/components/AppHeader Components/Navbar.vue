<template>

    <nav id="header-navbar">

        <!-- Avada Health Logo -->
        <img src="../../assets/img/medical_logo_2x_light.png" alt="Avada Health Logo">

        <!-- Unordered list with site pages links (dynamically generated) and Make Appointment button -->
        <ul>
            <li class="links" v-for="(link, index) in sitePages">
                <a :href="link.link">{{ link.text }}</a><span v-if="index == 2"><i class="fa-solid fa-angle-down"></i></span>

                <!-- Dropdown menu with unordered list containing departments links (dynamically generated) -->
                <ul class="departments-dropdown-menu" v-if="index == 2">
                    <li v-for="department in departments"><a :href="department.link">{{ department.text }}</a></li>
                </ul>
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
        padding: .5rem 4rem 3rem;
        color: $white;

        img {
            width: 250px;
            cursor: pointer;
        }

        ul {
            @include flex(row, space-between, center, no-wrap);

            li.links {
                font-family: 'Montserrat', sans-serif;
                padding: 0 0 3rem;
                margin: 3rem 1.5rem 0;
                text-transform: uppercase;
                cursor: pointer;
                font-size: .9rem;

                &:hover ul.departments-dropdown-menu {
                    opacity: 1;
                    z-index: 1;
                }

                & a,
                & span i {
                    transition: all .3s;
                }

                &:hover a,
                &:hover span i {
                    color: $teal;
                }

                &:first-child a {
                    color: $teal;
                }

                span {
                    margin-left: .5rem;
                }

                ul.departments-dropdown-menu {
                    @include flex(column, start, start, no-wrap);

                    margin: 1rem 0;
                    background-color: $white;
                    position: absolute;
                    opacity: 0;
                    transition: all .3s;

                    li {
                        padding: 1.5rem 1rem;
                        width: 100%;
                        text-transform: capitalize;
                        transition: all .3s;

                        &:hover {
                            background-color: $teal;
                        }

                        &:hover a {
                            color: $white;
                        }

                        a {
                            color: black;
                        }
                    }
                }
            }

            li button {
                background-color: $teal;
                transition: all .2s;
                margin: 0 1rem;
                font-size: .9rem;

                &:hover {
                    background-color: $blue;
                }
            }
        }
    }
</style>