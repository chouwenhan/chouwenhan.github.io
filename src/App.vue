<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <teheader :totitle='totitle' :fromtitle='fromtitle' :showbar='showBar' :name="transitionName"></teheader>
    <router-view/>
  </div>
</template>
<script>
import teheader from './components/teheader.vue'
export default {
  name: 'App',
  components: {
    teheader
  },
  data () {
    return {
      totitle: true,
      fromtitle: true,
      showBar: true,
      transitionName: true
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
body {
  margin: 0px;
}
</style>
