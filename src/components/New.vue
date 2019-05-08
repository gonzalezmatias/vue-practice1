<template>
    <div>
        <button @click="counter++">incrase</button>
        <h3>New Quote!</h3>
        <p>{{counter}}</p>
    </div>
</template>

<script>
export default {
    data: function (){
        return{
            counter:0
        };
    }
}
</script>

<style scoped>

</style>
