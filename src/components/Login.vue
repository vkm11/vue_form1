<template>
  <div>
    <input type="text" v-model="loginForm.username" name="username" placeholder="Enter user name"/><br /><br />
    <input type="password" v-model="loginForm.password" name="password" placeholder="Enter password" /><br /><br />
    <button v-on:click="loginData">Login</button>
  </div>
</template>

<script>
export default {
  name: "Login-form",
  methods: {
    loginData() {
      console.log("Login Data",this.loginForm.username,this.loginForm.password);
    }
  },
  data() {
      return {
        loginForm: {
          username: null,
          password: null,
        }
      }
    }
}
</script>