<template>
    <div id="appointment-form">
        
        <!-- Upper title section -->
        <div class="title">
            <h2>Make An Appointment</h2>
            <hr>
            <p>Sed Ut Perspiciatis Unde Omnis Iste Natus Error Sit Voluptatem Accusantium Doloremque Laudantium, Totam Rem Aperiam, Eaque Ipsa Quae Ab Illo Inventore Veritatis Et Quasi Architecto Beatae</p>
        </div>

        <!-- Bottom appointment form section -->
        <div class="form">
            <input type="text" placeholder="Name*" required>
            <input type="email" placeholder="Email*" required>
            <input type="text" placeholder="Phone Number">
            <div class="appointment-date">
                <i class="fa-solid fa-calendar-days"></i>
                <input type="text" placeholder="Appointment Date">
            </div>
            <textarea rows="4" placeholder="How can we help?*" required></textarea>
            <button>Make an appointment</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppointmentForm'
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;
    
    div#appointment-form {
        text-align: center;
        padding: 9rem 0 10rem;
        background-image: url('../../assets/img/make-an-appointment.jpg');
        background-position: 0 50%;
        background-size: cover;
        color: white;

        div.title {
            margin-bottom: 1.5rem;

            h2 {
                font-size: 2.7rem;
                color: $white;
            }

            p {
                color: $white;
            }
        }

        div.form {
            width: 40%;
            margin: auto;

            input,
            textarea {
                margin: 1rem;
                background-color: transparent;
                color: grey;
                padding: 1rem;
                border: 1px solid $white;

                &:hover {
                    border-color: #286978;
                }

                &:focus {
                    border: none;
                    outline: 1px solid $teal;
                }
            }

            input {
                width: calc(100% / 2 - 2rem);
            }

            textarea {
                width: calc(100% - 2rem);
                margin-bottom: 1.5rem;
            }

            div.appointment-date {
                position: relative;
                display: inline;

                input {
                    padding-left: 2rem;
                }

                i.fa-calendar-days {
                    position: absolute;
                    top: 3px;
                    left: 27px;
                    color: grey;
                    font-size: .8rem;
                }
            }

            button {
                width: calc(100% - 2rem);
                color: $white;
                background-color: $teal;
                transition: all .2s;

                &:hover {
                    background-color: $blue;
                }
            }
        }
    }
</style>