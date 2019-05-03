<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <p>User name: {{switchName()}}</p>
        <p>User age: {{userAge}}</p>
        <button @click="resetName">Reset name</button>
    </div>
</template>

<script>
    import {eventBus} from '../main';

    export default{ //validate props!! props cant be multiple Types ej [String, Array, other types] and can be an object
        props: {
            name:{
                type: String,
                required: true //only works if the props is passed 
                // defautl:'some name' you can also add a default value, but is dont have sense with the required 
            },
            userAge:{
                type: Number,
                defautl: 0
            }
        }, 
        methods:{
            switchName (){
                return this.name.split("").reverse().join("");
            },
            resetName (){
                this.name = "Matias";
                this.$emit('nameWasReset', this.name); // $emet, this sentece is to pass data from the children to the parent component
            }
        },
        created(){
            eventBus.$on('ageUpdate', (data) =>{ //data is just a name i can use whatever i want
                this.userAge = data;
            })
        }

    }
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
