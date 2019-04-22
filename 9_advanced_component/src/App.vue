<template>
    <div class="container">
        <div class="row">
            <div class="col-lg-12">
                <button @click="selectedComponent = 'appQuote'">Quote</button>
                <button @click="selectedComponent = 'appAuthor'">Author</button>
                <button @click="selectedComponent = 'appNew'">New</button>
                <hr>
                {{ selectedComponent }}
                <keep-alive>
                    <component :is="selectedComponent">
                        <p>Default Content</p>
                    </component>
                </keep-alive>
                <!-- <app-quote>
                    <strong slot="title">{{ theQuote }}</strong>
                    <p>{{ theParagraph }}</p>
                </app-quote> -->
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
    import New from './components/New.vue';
    import Author from './components/Author.vue';
    export default {
        data: function() {
            return {
                theQuote: 'Hello World',
                selectedComponent: 'appQuote'
            }
        },
        components: {
            appQuote: Quote,
            appNew: New,
            appAuthor: Author
        }
    };
</script>

<style>
</style>
