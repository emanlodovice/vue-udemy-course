<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <p>User Name: {{ switchName() }}</p>
        <p>User Age: {{ userAge }}</p>
        <button @click="resetName">Reset The Name</button>
        <button @click="resetFn()">Reset The Name</button>
    </div>
</template>

<script>
    export default {
        props: {
            myName: {
                type: String,
                required: false,
                default: 'Nice ka',
            },
            resetFn: Function,
            userAge: Number
        },
        methods: {
            switchName() {
                return this.myName.split('').reverse().join('');
            },
            resetName() {
                this.myName = 'Eman updated';
                this.$emit('nameWasReset', this.myName);
            }
        }
    }
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
