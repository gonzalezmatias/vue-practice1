<template>
    <div>
       <server-status v-for="server in 5">{{ server }}</server-status>
    </div>
</template>

<script>
    import ServerStatus from './ServerStatus.vue';
    export default {
        components:{
            'server-status': ServerStatus
        }
       
    }
</script>



<style></style>