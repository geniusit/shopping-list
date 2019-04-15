<template>
    <h1>{{ msg }} {{user}}</h1>
</template>

<script>
    export default {
        data () {
            return {
                msg: 'Hello!'
            }
        },
        props: ['user']
    }
</script>