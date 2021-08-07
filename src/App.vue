<template>
  <div id="nav">
    <router-link to="/">Home</router-link>
    <router-link to="/search-detail">Search Detail</router-link>
  </div>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 15px 20px;
  border-radius: 10px;
  transition: all 0.2s ease-in-out;
}

#nav a:first-child {
  margin-right: 20px;
}

#nav a:hover {
  background-color: #a9cebd;
  color: white;
}

#nav a.router-link-exact-active {
  color: white;
  background-color: #42b983;
}
</style>
