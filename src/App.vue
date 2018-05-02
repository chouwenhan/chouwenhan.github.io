<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <teheader :totitle='totitle' :fromtitle='fromtitle' :showbar='showBar' :name="transitionName"></teheader>
    <router-view/>
  </div>
</template>
<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-118588196-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-118588196-1');
</script>
<script>
import teheader from './components/teheader.vue'
export default {
  name: 'App',
  components: {
    teheader
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
