<template>
    <div class="container">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-grid :quotes="quotes" @quoteDeleted="deletQuote"></app-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Info: click on a QUote to delet it!</div>
            </div>
        </div>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue'
    import NewQuote from './components/NewQuote.vue'
    import Header from './components/Header.vue'

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
            appGrid: QuoteGrid,
            appNewQuote : NewQuote,
            appHeader : Header
        },
        methods:{
            newQuote(quote){
                if (this.quotes.length >= this.maxQuotes ){
                    return alert("delete somo quotes")
                } 
                this.quotes.push(quote)
            },
            deletQuote(index){
                this.quotes.splice(index, 1);
            }
        }
    }
</script>

<style>
</style>
