<template>
    <header>
        <!-- Navbar Component -->
        <Navbar
            :sitePages="sitePages"
            :departments="departments"
        />

        <!-- Central info section -->
        <div id="header-info">

            <!-- Left-side section with title -->
            <div class="title">
                <h1>Caring <span>For Life</span></h1>
                <p>Kind words can be short and easy to speak, but their echoes are truly endless. Avada Health focuses on you as if it was our own family.</p>
                <button><a href="#">Learn more</a></button>
            </div>

            <!-- Right-side section with office hours table -->
            <div class="office-hours">
                <span>Office Hours</span>
                <hr>
                <table>
                    <tr>
                        <td>Monday - Friday</td>
                        <td>8:00 - 5:00</td>
                    </tr>
                    <tr>
                        <td>Saturday</td>
                        <td>9:00 - 5:00</td>
                    </tr>
                    <tr>
                        <td>Sunday</td>
                        <td>11:00 - 4:00</td>
                    </tr>
                </table>
                <span>+44(0) 1865 339665</span>
            </div>
        </div>
    </header>
</template>

<script>
import Navbar from './AppHeader Components/Navbar.vue';
export default {
    name: 'AppHeader',

    components: {
        Navbar
    },
    
    props: {
        sitePages: Array,
        departments: Array
    }
}
</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    
    header {
        background-image: url('../assets/img/header-image-homepage.jpg');
        background-size: 120%;
        background-position: 60% 0;

        div#header-info {
            @include flex(row, center, center, no-wrap);
            width: 65%;
            margin: auto;
            padding: 12rem 0;
            color: $white;
            transform: translate(-1%, -11%);
            
            div.title {
                width: 70%;

                h1 {
                    font-size: 5.5rem;
                    font-weight: 400;

                    span {
                        color: $teal;
                    }
                }

                p {
                    font-size: 1.7rem;
                    margin: 1rem 0;
                    width: 95%;
                    line-height: 35px;
                    color: $white;
                }

                button {
                    background-color: $teal;
                    color: $white;
                    margin: 1.5rem 0;
                    font-size: 1.2rem;
                    padding: 1rem 3rem;
                    transition: all .2s;

                    &:hover {
                        background-color: $blue;
                    }
                }
            }

            div.office-hours {
                width: 30%;
                background-color: #3bb0bf80;
                padding: 1rem;
                text-align: center;
                margin-left: 2rem;

                span {
                    text-transform: uppercase;
                    display: inline-block;
                    padding: 1.5rem;
                    font-size: 1.4rem;
                }

                hr {
                    border: 2px solid $teal;
                    margin-bottom: 1rem;
                }

                table tr td {
                    padding: 1.5rem 1.7rem 1.5rem;
                    text-align: start;
                }
            }
        }
    }
</style>