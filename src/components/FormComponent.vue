<template id="form">
    <div>
        <label for="name">What's your name?</label>
        <input v-bind:value="value" type="text" id="name" v-on:input="onInput" />
    </div>
</template>

<script>
    export default {
        props: {
            value:String
        },
        methods: {
            onInput: function(event) {
                this.$emit('input', event.target.value)
            }
        }
    }
</script>