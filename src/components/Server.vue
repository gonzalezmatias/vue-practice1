<template>
 <div class="col-xs-12 col-sm-6">
                <ul class="list-group">
                    <li
                            class="list-group-item"
                            v-for="index in 4"
                             v-bind:key="index">
                        Server #{{ index }} <app-status></app-status>
                    </li>
                </ul>
            </div>
</template>

<script>
    import ServerStatus from './ServerStatus.vue';
    export default{
        components:{
            'app-status' : ServerStatus
        }
    }

</script>

<style scoped>
    div{
        border: 1px solid blue;
    }
</style>

