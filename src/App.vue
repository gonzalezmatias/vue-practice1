<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
               <app-quote>
                   <h2 slot="title">{{ quoteTitle }}</h2> <!-- only the style is setup in te child, others comprtamientos it's change here -->
                   <p>Somo quote by Slot</p>
               </app-quote>
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
    export default {
        data: function(){
            return{
                quoteTitle: 'Somo title from data'
            }
        },
        components: {
            appQuote: Quote
        }
    }
</script>


<style scoped>

</style>
