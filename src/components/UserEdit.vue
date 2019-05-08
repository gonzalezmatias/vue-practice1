<template>
    <div class="component">
        <h3>You may edit the User here</h3>
        <p>Edit me!</p>
        <p>User Age: {{userAge}}</p>
        <button @click="editAge">Edit age</button>
    </div>
</template>

<script>
    import { eventBus } from '../main';

    export default{
        props:{
            userAge:{
                type: Number,
                default: 0
            }
        },
        methods:{
            editAge (){
                this.userAge= 30;
               // this.$emit('ageUpdate', this.userAge) this is used 4 pass data to thye parent
               //eventBus.$emit('ageUpdate', this.userAge);
                eventBus.changeAge(this.userAge);
            }
        }
    }
</script>

<style scoped>
    div {
        background-color: lightgreen;
    }
</style>
