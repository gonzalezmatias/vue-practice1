<template>
    <div class="container">
        <app-grid :quotes="quotes"></app-grid>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue'
    export default {
        data: function(){
            return{
                quotes: [
                    'Example quote'
                ],
                maxQuotes: 10
            } 
        },
        components:{
            appGrid: QuoteGrid
        }
    }
</script>

<style>
</style>
