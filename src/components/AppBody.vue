<template>
    <AppHeader
        :sitePages="sitePages"
        :departments="departments"
    />
    <AppMain />
    <AppFooter />
</template>

<script>
import AppHeader from './AppHeader.vue';
import AppMain from './AppMain.vue';
import AppFooter from './AppFooter.vue'
export default {
    name: 'AppBody',

    components: {
        AppHeader,
        AppMain,
        AppFooter
    },

    data() {
        return {
            sitePages: [
                {
                    text: 'Home',
                    link: '#'
                },
                {
                    text: 'About',
                    link: '#'
                },
                {
                    text: 'Departments',
                    link: '#'
                },
                {
                    text: 'Articles',
                    link: '#'
                }
            ],

            departments: [
                {
                    text: 'General Practice',
                    link: '#'
                },
                {
                    text: 'Cardiology',
                    link: '#'
                },
                {
                    text: 'Pediatrics',
                    link: '#'
                },
                {
                    text: 'Diabetes Care',
                    link: '#'
                },
                {
                    text: 'Pre-natal Care',
                    link: '#'
                },
                {
                    text: 'Ultrasound Echocardiogram',
                    link: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    
</style>