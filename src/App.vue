<template>
 
    <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{name:'about'}">About</router-link>
    <router-link :to="{name:'login'}">Login</router-link>
    <router-link :to="{name:'SignUp'}">Signup</router-link>
    <router-link :to="{name:'Products'}">Products</router-link>
    </nav>
  <router-view/>

</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #3b6085;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #3a6087;
  text-decoration:none;
  font-size:2em;
}

nav a.router-link-exact-active {
  color:rgb(219, 112, 149);
  background-color:rgb(57, 42, 42);
  border-radius:0.25rem;
 padding:10px 10px;
  margin:auto 0.5rem
}
</style>
