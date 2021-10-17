<template>
  <div id="app">
    <Header/>
    <Card/>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header";
import Card from './components/Card';
import Footer from "./components/Footer";

export default {
  name: 'App',
  components: {
    Header,
    Card,
    Footer,
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
  overflow: scroll;
}

</style>
