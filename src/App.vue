<template>
  <MainPage></MainPage>
  <AboutPage></AboutPage>
  <CollectionPage></CollectionPage>
  <BikePage></BikePage>
</template>

<script>
import MainPage from './components/MainPage.vue'
import AboutPage from './components/AboutPage.vue'
import CollectionPage from './components/CollectionPage.vue'
import BikePage from './components/BikePage.vue'
export default {
  name: 'App',
  components: {
    MainPage,
    AboutPage,
    CollectionPage,
    BikePage

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
