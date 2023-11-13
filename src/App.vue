<template>
  <MainPage></MainPage>
  <AboutPage></AboutPage>
</template>

<script>
import MainPage from './components/MainPage.vue'
import AboutPage from './components/AboutPage.vue'

export default {
  name: 'App',
  components: {
    MainPage,
    AboutPage
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
</style>
