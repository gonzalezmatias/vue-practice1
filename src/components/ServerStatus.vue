<template>
    <div>
        <p>Server Status: {{server}}</p>
        <hr>
        <button @click="changeStatus"> change status</button>    
    </div>
</template>

<script>
    export default {
        data: function (){
            return{
                server : 'critical'
            }
        },
        methods:{
            changeStatus: function (){
                this.server = 'normal';
            }
        }
    }
</script>



<style></style>