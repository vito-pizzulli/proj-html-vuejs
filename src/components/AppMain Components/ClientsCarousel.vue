<template>
    <div id="clients-carousel">
        <ClientLogo />
    </div>
</template>

<script>
import ClientLogo from './ClientLogo.vue'
export default {
    name: 'Clients',

    components: {
        ClientLogo
    }
}
</script>

<style lang="scss" scoped>
    
    div#clients-carousel {
        background-image: url(../../assets/img/rgb-gradient-bar-for-logo-carrasel.jpg);
        height: 300px;
    }
</style>