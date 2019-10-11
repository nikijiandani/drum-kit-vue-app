<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Poushita msg="Welcome to Poushita's Vue.js App"/>
    <PerrysComponent msg="Hello, my name is Perry and this is my component"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Poushita from "./components/Poushita.vue";
import PerrysComponent from './components/PerrysComponent.vue'

export default {
  name: "app",
  components: {
    HelloWorld,
    Poushita,
    PerrysComponent
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
