<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->

  <!-- v-bind -> : is sending the value as a Number type ot expression 
  15 + 15 for example -->
  <!-- <Counter :start="99" /> -->

  
  <Indecision />
</template>

<script>
// import Counter from "./components/Counter.vue";
import Indecision from "./components/Indecision.vue";
export default {
  name: "App",
  components: {
    // Counter,
    Indecision,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
