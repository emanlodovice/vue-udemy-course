<template>
    <div>
        <h3>New Quote</h3>
        <button @click="counter++">Increase</button>
        {{ counter }}
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                counter: 1
            }
        },
        destroyed: function() {
            console.log('destroyed');
        },
        deactivated() {
            console.log('deactivated')
        },
        activated() {
            console.log('activated')
        }
    };
    
</script>

<style scoped>
</style>