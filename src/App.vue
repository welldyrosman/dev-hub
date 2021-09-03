<template>
  <div id="app">
    <TopMenu/>
    <Navbar/>
    <Login msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import TopMenu from './components/Template/TopMenu.vue'
import Navbar from './components/Template/Navbar.vue'
import Login from './components/Login'

export default {
  name: 'App',
  components: {
    Login,TopMenu,Navbar
  }
}
</script>

<style>
</style>
