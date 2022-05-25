<template>
  <div id="app">
    <!-- <h1>Make form in vue js</h1> -->
    <h2>form validation</h2>
    <!-- <Login /> -->
    <Login_validation />
  </div>
</template>

<script>
// import Login from "./components/Login";
import Login_validation from "./components/Login_validation";
export default {
  name: "App",
  components: {
    // Login,
    Login_validation
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
