<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Portfolio from "./components/Portfolio.vue";
</script>

<template>
  <div id="app">
    <HelloWorld />
    <Portfolio />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Portfolio,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
body {
  margin: 0;
  padding: 0;
}
#app {
  /* Add styles here */
}
</style>

<!-- -->