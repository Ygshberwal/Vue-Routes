<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{name:'About'}">About</router-link> |
    <router-link :to="{name:'Jobs'}">Jobs</router-link> 
  </nav>
  <button @click="back"> &#8249;</button>
  <button @click="redirect">Redirect</button>
  <button @click="forward">&#8250;</button>
  <router-view/>
</template>

<script>
export default{
  methods:{
    back() {
      this.$router.go(-1)
    },
    redirect() {
      this.$router.push({name:'Home'})
    },
    forward() {
      this.$router.go(1)
    }
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
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
button{
  text-decoration: none;
  display: inline-block;
  padding: 8px 16px;
  border: none;
  color:white;
  margin: 0 5px;
  background-color: #42b983;
  border-radius: 100px;
}
</style>
