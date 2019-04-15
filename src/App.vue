<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>

    <hello-component :user="user"></hello-component>
    <shopping-list></shopping-list>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HelloComponent from './components/HelloComponent'
import ShoppingList from './components/ShoppingList'


export default {
  name: 'app',
  data () {
    return {
      user: 'nnn'
    };
  },
  components: {
    HelloWorld,
    HelloComponent,
    ShoppingList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
