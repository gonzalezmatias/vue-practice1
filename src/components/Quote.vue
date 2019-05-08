<template>
    <div>
        <div class="title">
            <slot name="title"></slot>
            <span style=" color: #ccc"><slot name="subTitle">The Subtitle</slot></span>
        </div>
        <hr>
        <div>
            <slot></slot>
        </div>

        <p>outside the slot</p>
    </div>    
</template>

<script>
export default {
    props:['quote']
}
</script>

<style scoped>
        div{
        border: 1px solid #ccc;
        box-shadow: 1px 1px 2px black;
        padding: 30px;
        margin: auto; 
    }

        h2{
            color: red;
        }

        .title{
            font-style: italic;
        }
</style>
