<template>
  <div id="app">
    <Slogan/>
    <Card/>
  </div>
</template>

<script>
import Slogan from "./components/Slogan";
import Card from './components/Card';

export default {
  name: 'App',
  components: {
    Slogan,
    Card,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');
@import './assets/icons/icomoon/styles.min.css';
@import './assets/css/all.min.css';

html {
  background-color: #F5F5F5;
}

#app {
  text-align: center;
}
</style>
