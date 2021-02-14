<template>
  <div id="app">
    <main-menu/>
    <router-view/>
  </div>
</template>

<script>
import MainMenu from '@/components/card/MainMenu'

export default {
  components: { MainMenu },
  name: 'App',

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
</style>
