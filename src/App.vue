<template>
    <NavBar/>
  <div>
    <homepage v-show="showHomePage" @close="closeHomepage"/>
    <installingVue v-show="showInstallPage" @next="changePage1"/>
    <createVueApp v-show="nextPage1" @next1="changePage2"/>
    <conditionalRendering v-show="nextPage2" @next2=""/>
  </div>
</template>

<script>
import Homepage from "./components/HomePage.vue"
import installingVue from './components/installingVue.vue'
import NavBar from './components/NavBar.vue'
import createVueApp from "./components/createVueApp.vue"
import conditionalRendering from './components/conditionalRendering.vue'


export default {
  name: 'App',
  components: {
    Homepage,
    NavBar,
    installingVue,
    createVueApp,
    conditionalRendering,
  },
  data() {
    return {
      showHomePage: true,
      showInstallPage: false,
      nextPage1: false,
      nextPage2: false,
    }
  },
  methods: {
    closeHomepage(name) {
      this.showInstallPage = true,
      this.showHomePage = false,
      console.log('name', name)
    },
    changePage1(name) {
      this.nextPage = true,
      this.showInstallPage = false,
      console.log('name', name)
    },
    changePage2(name) {
      this.nextPage = false;
      console.log('name', name)
    },
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
