<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar></Navbar>
    <Hook></Hook>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Hook from "./components/Hook.vue";

export default {
  name: "App",
  data() {
    return {
      title: "How Are You Endi Julian",
    };
  },
  components: {
    Navbar,
    Hook,
  },
  methods: {},
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
