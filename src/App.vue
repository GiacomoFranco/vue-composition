<template>
  <UserRepositories :user="'@francoder_'"/>
  <Home :first-name="'Santy'" :last-name="'Gil'" otro="algo"></Home>
</template>

<script>
import UserRepositories from './components/UserRepositories.vue';
import Home from './components/Home.vue';
import { provide } from 'vue';


export default {
  name: 'App',
  components: {
    Home,
    UserRepositories
  },
  setup() {
    provide('username', '@francoder_____')
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
