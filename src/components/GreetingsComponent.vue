<template id="greetings">
    <div>
        <h1>Greetings component</h1>
        <form-component v-model="user"></form-component>
        <hello-component :user="user"></hello-component>
    </div>
</template>
<script>

    import HelloComponent from './HelloComponent'
    import FormComponent from './FormComponent'

    export default {
        data: function () {
            return {
                user: 'hero'
            }
        },
        components: {
            HelloComponent,
            FormComponent
        }
    }
</script>