<template>

    <!-- Copyright info-->
    <div id="copyright">
        <p>&#169; Copyright 2012-2023 | <a href="#">Avada Website Builder</a> by <a href="#">ThemeFusion</a> | All Rights Reserved by <a href="#">WordPress</a></p>
    </div>
</template>

<script>
export default {
    name: 'Copyright'
}
</script>

<style lang="scss" scoped>
    @use '../../styles/partials/variables' as *;
    
    div#copyright {
        background-color: $light_grey;
        color: grey;
        padding: 2.5rem 7rem;

        p a {
            color: black;
        }
    }
</style>