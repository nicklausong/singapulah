<template>
  <div>
    <div id="app" v-if="notLoggedIn == true">
      <router-link :to="{ name: 'Home' }">
        <button type="button" v-on:click="notLoggedIn = false">Login</button>
      </router-link>
      <router-view></router-view>
    </div>
    <div id="app" v-if="notLoggedIn != true">
      <router-link :to="{ name: 'Home' }">LOGGED IN</router-link>
      <router-link :to="{ name: 'Rank' }">Rank Friends!</router-link>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      notLoggedIn: true
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
