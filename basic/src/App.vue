<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar></Navbar>
    <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Post</a></li>
        <li><a href="">About</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
  import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  data(){
    return{
      title: 'How Are You Endi Julian'
    }
  },
  components: {
    Navbar
  }
}
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
