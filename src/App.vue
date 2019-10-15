<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <NikiJiandani msg="Hello from Niki's component!"/>
    <PerrysComponent msg="Hello, my name is Perry and this is my component"/>
    <Poushita msg="Welcome to Poushita's Vue Component"/>
  </div>
</template>

<script>
import NikiJiandani from "./components/NikiJiandani.vue";
import PerrysComponent from "./components/PerrysComponent.vue";
import Poushita from "./components/Poushita.vue";

export default {
  name: "app",
  components: {
    NikiJiandani,
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
