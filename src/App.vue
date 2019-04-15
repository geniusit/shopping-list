<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>

    <greetings-component></greetings-component>
    <shopping-list></shopping-list>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

import ShoppingList from "./components/ShoppingList";
import GreetingsComponent from "./components/GreetingsComponent";

export default {
  name: "app",
  data() {
    return {
      user: "nnn"
    };
  },
  components: {
    HelloWorld,
    ShoppingList,
    GreetingsComponent
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
