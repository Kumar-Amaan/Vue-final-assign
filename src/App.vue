<template>
  <div itemid="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/dashboard">Dashboard</router-link> |
      <router-link to="/register">Register</router-link> |
      <router-link to="/userdetails">User-Details</router-link>
      <!-- <router-link to="/vuex">Vuex</router-link> -->
    </div>
    <router-view />
  </div>
</template>
<style scope>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 13px;
  position: relative;
  /* left: 40%; */
  width: 100%;
  bottom: 6px;
  background-color: rgb(51, 40, 40);
}

#nav a {
  font-weight: bold;
  color: #1d0518;
  background-color: rgb(64, 215, 241);
  border: 2px solid rgb(33, 39, 41);
  border-radius: 5px;
}

#nav a.router-link-exact-active {
  color: #160704;
}
</style>