<template>
  <div id="app">
    <Header/>
    <Select/>
    <Card/>
    <Mobile/>
    <Apple/>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header";
import Select from "./components/Select";
import Card from './components/Card';
import Mobile from "./components/Mobile";
import Apple from "./components/Apple";
import Footer from "./components/Footer";

export default {
  name: 'App',
  components: {Header, Select, Card, Mobile, Apple, Footer},
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');
@import './assets/icons/icomoon/styles.min.css';
@import './assets/css/all.min.css';

#app {
  text-align: center;
  overflow-y: scroll;
  overflow-x: hidden;
  min-height: 100%;
  position: relative;
}
</style>
