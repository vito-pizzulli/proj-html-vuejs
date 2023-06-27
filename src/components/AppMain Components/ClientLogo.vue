<template>
    <div class="client-logo">
        <img :src="client.logo" alt="Client Logo">
    </div>
</template>

<script>
export default {
    name: 'ClientLogo',

    props: {
        client: Object
    }
}
</script>

<style lang="">
    
</style>