<template>
    <div id="about-us">
        <div class="left-section">
            <img src="../../assets/img/medical_logo_1x_dark.png" alt="Avada Health Logo Small">
            <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolemue launti totam aperiam, eaque ipsa quae abillo. Ivente veriatis et quasi architecto beatae luptatem accusantium, remaperiamsiat.Voluptatem accusest etsium doloremque laudaien. Lorem ipsum sits dolores ets unser.</p>
            <h3>Learn more about us</h3>
            <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-instagram"></i></a>
            <a href="#"><i class="fa-brands fa-youtube"></i></a>
        </div>
        <div class="central-section">
            <h3>Contact Information</h3>
            <hr>
            <span>121 King Street, London United Kingdom</span>
            <span>1.800.458.556</span>

            <div class="google-maps">
                <span>For privacy reasons Google Maps needs your permission to be loaded.</span>
                <button>I Accept</button>
            </div>
        </div>
        <div class="right-section">
            <h3>Medical departments</h3>
            <hr>
            <ul>
                <li v-for="department in departments"><a :href="department.link"><i class="fa-solid fa-circle-check"></i> {{ department.text }}</a></li>
            </ul>
            <button>View Our Departments</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AboutUs',

    props: {
        departments: Array
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;

    div#about-us {
        @include flex(row, start, start, no-wrap);
        padding: 5rem 3rem;

        div.left-section,
        div.central-section,
        div.right-section {
            width: calc(100% / 3);
            margin: 0 2rem;

            h3 {
                text-transform: uppercase;
                font-weight: 400;
                font-size: 1.2rem;
                margin-bottom: 1.5rem;
            }

            hr {
                color: $teal;
                width: 45px;
                margin-bottom: 1.5rem;
            }

            p,
            span {
                color: grey;
                margin-bottom: 1.5rem;
            }

            p {
                line-height: 35px;
            }

            span {
                display: block;
            }

            button {
                background-color: $teal;
                color: white;
                width: 100%;
            }
        }

        div.left-section h3 {
            margin-bottom: 2rem;
        }

        div.central-section div.google-maps {
            background-color: $lighter_grey;
            text-align: center;
            padding: 2rem 1.5rem;
        }

        div.right-section ul {
            margin-bottom: 2rem;

            li {
                margin: .5rem 0;

                a {
                    color: grey;

                    i {
                        color: $teal;
                        font-size: 2rem;
                    }
                }
            }
        }
    }
</style>