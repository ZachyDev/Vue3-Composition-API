<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <TestVue3 msg="Welcome to Your Vue.js App"/>
    <Test2 />
  </div>
  
</template>

<script>
import TestVue3 from './components/TestVue3.vue'
import Test2 from '@/components/Test2.vue'
export default {
  name: 'App',
  components: {
    TestVue3,
    Test2
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
