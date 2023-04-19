<template>
  <UserRepositories :user="'@francoder_'"/>
  <Home :first-name="'Santy'" :last-name="'Gil'"></Home>
</template>

<script>
import UserRepositories from './components/UserRepositories.vue';
import Home from './components/Home.vue';

export default {
  name: 'App',
  components: {
    Home,
    UserRepositories
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
