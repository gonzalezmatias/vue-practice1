<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <button @click="selectedComponent = 'appQuote'">Quote</button>
                <button @click="selectedComponent = 'appAuthor'">Author</button>
                <button @click="selectedComponent = 'appNew'">New</button>
                <hr>
                <p>{{selectedComponent}}</p>
                <keep-alive>
                    <component :is="selectedComponent"></component>
                </keep-alive>
                
               <!-- <app-quote>
                   <h2 slot="title">{{ quoteTitle }}</h2> 
                   <p>Somo quote by Slot</p>
               </app-quote> -->
               <!-- only the style is setup in te child, others comprtamientos it's change here -->
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
    import Author from './components/Author.vue';
    import New from './components/New.vue';
    export default {
        data: function(){
            return{
                quoteTitle: 'Somo title from data',
                selectedComponent: 'appQuote'
            }
        },
        components: {
            appQuote: Quote,
            appAuthor: Author,
            appNew: New
        }
    }
</script>


<style scoped>

</style>
