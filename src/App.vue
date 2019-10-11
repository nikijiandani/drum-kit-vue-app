<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <NikiJiandani msg="Hello from Niki's component!" />
    <PerrysComponent msg="Hello, my name is Perry and this is my component" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import NikiJiandani from "./components/NikiJiandani.vue";
import PerrysComponent from "./components/PerrysComponent.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    NikiJiandani,
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
