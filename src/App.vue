<template>
  <div id="app">
    <Logo/>
    <Card msg=""/>
  </div>
</template>

<script>
import Card from './components/Card'
import Logo from './components/Logo'

export default {
  name: 'App',
  components: {
    Card,
    Logo,
  }
}
</script>

<style>
html {
  background-color: #F5F5F5;
}

#app {
  text-align: center;
}
</style>
