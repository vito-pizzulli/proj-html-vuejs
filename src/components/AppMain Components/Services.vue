<template>
    <div id="services">

        <!-- Upper title section -->
        <div class="title">
            <img src="../../assets/img/icon-6.png" alt="Services Icon">
            <h2>Our Health Services</h2>
            <hr>
            <p>Sed Ut Perspiciatis Unde Omnis Iste Natus Error Sit Voluptatem Accusantium Doloremque Laudantium, Totam Rem Aperiam, Eaque Ipsa Quae Ab Illo Inventore Veritatis Et Quasi Architecto Beatae</p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Services'
}
</script>
<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    @use '../../styles/partials/mixins' as *;

    div#services {
        text-align: center;
        padding: 7rem 0 5rem;

        div.title h2 {
            text-transform: uppercase;
        }
    }
</style>