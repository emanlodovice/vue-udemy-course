<template>
    <div class="container">
        <div class="row">
            <div class="col-lg-12">
                <app-quote>
                    <strong slot="title">{{ theQuote }}</strong>
                    <p>{{ theParagraph }}</p>
                </app-quote>
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
    export default {
        data: function() {
            return {
                theQuote: 'Hello World',
                theParagraph: 'paragraph'
            }
        },
        components: {
            appQuote: Quote
        }
    };
</script>

<style>
</style>
