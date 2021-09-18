<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/112.jpg" width="500" height="410"> 
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <faculty/>
    <test/>
  </div>
</template>

<script>
import Vue from "vue";
import faculty from './components/faculty.vue'
import HelloWorld from './components/HelloWorld.vue'
import {BootstrapVue , IconsPlugin} from 'bootstrap-vue'
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
import Test from './components/Test.vue';


Vue.use(BootstrapVue);
Vue.use(IconsPlugin);

export default {
  name: 'App',
  components: {
    HelloWorld,
    faculty,
    Test,
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
