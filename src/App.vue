<template>
  <div id="app">
    <VuetifyTest msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import VuetifyTest from "./components/VuetifyTest.vue";

export default {
  name: "App",
  components: {
    VuetifyTest,
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
