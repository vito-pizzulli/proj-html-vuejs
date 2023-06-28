<template>

    <!-- Clients logo carousel, populated by ClientLogo Components -->
    <div id="clients-carousel">
        <div class="container">
            <ClientLogo v-for="client in clients"
                :client="client"
            />
        </div>
    </div>
</template>

<script>
import ClientLogo from './ClientLogo.vue'
export default {
    name: 'Clients',

    components: {
        ClientLogo
    },

    data() {
        return {
            clients: [
                {
                    logo: './src/assets/img/client-logos-1.png'
                },
                {
                    logo: './src/assets/img/client-logos-2.png'
                },
                {
                    logo: './src/assets/img/client-logos-3.png'
                },
                {
                    logo: './src/assets/img/client-logos-4.png'
                }
            ]
        }
    },

    created() {
        setInterval(() => {
            this.clients.push(this.clients.shift());
        }, 4000);
    }
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/mixins' as *;
    
    div#clients-carousel {
        background-image: url(../../assets/img/rgb-gradient-bar-for-logo-carrasel.jpg);
        padding: 2.5rem 0;

        div.container {
            @include flex(row, center, center, no-wrap);
            width: 70%;
            margin: auto;
        }
    }
</style>