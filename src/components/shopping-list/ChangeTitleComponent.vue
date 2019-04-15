<template id="change-title-template">
    <div>
        <em>Change the title of your shopping list here</em>
        <input v-bind:value="value" v-on:input="onInput" >
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