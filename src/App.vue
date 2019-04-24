<template>
    <div class="container">
        <div class="row">
            <app-header></app-header>
        </div>
        <hr>
        <div class="row">
            <app-server></app-server>
            <app-details></app-details>            
        </div>
        <hr>
        <div class="row">
            <app-footer></app-footer>
        </div>
    </div>
</template>

<script>
    import Header from './Header.vue';
    import Footer from './Footer.vue';
    import Server from './Server.vue';
    import ServerDetails from './ServerDetails.vue';

    export default {
        components: {
            'app-header': Header,
            'app-footer' : Footer,
            'app-server': Server,
            'app-details': ServerDetails
        }
    }

</script>

<style>

</style>
