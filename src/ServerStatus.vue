<template>
    <div>
        <p v-bind:class="{danger : active}">Server Status: {{server}}</p>
        <hr>
        <button @click="changeStatus"> change status</button>    
    </div>
</template>

<script>
    export default {
        data: function (){
            return{
                server : 'critical',
                active : false
            }
        },
        methods:{
            changeStatus: function (){
                this.server = 'normal';
                this.active = true;
            }
        }
    }
</script>



<style>
.danger{
    color: red;
}

</style>