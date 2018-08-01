<template>
    <div class="container">
        <div class="row">
            <div class="col-lg-12">
                <app-quote><strong>{{ theQuote }}</strong></app-quote>
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
    export default {
        data: function() {
            return {
                theQuote: 'Hello World'
            }
        },
        components: {
            appQuote: Quote
        }
    };
</script>

<style>
</style>
