<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/jobs">Jobs</router-link>
  </div>

  <div class="historyButtons">
    <button @click="Redirect">Redirect</button>
    <button @click="back">Go back</button>
    <button @click="forward">Go forward</button>
  </div>

  <router-view/>
</template>

<script>
  export default {
    methods: {
      Redirect() {
        this.$router.push({ name: 'Home' })
      },
      back() {
        this.$router.go(-1)
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

  #nav {
    padding: 30px;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }

  .historyButtons button {
    font-size: .75rem;
    margin: 0 10px;
    padding: 10px 14px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
</style>
