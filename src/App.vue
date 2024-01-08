<template>
  <TheHeader v-if="showHeader"/>
  <div v-show="showName">
    <ol>
      <li>Nome: {{ name }}</li>
      <li>Sobrenome: {{ lastName }}</li>
    </ol>
  </div>

  <div v-if="accessLevel === 'admin'">Admin</div>
  <div v-else-if="accessLevel === 'market'">Marketing</div>
  <div v-else>Normal</div>

  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue';

export default {
  name: 'App',
  components: {
    HelloWorld, TheHeader
  }, 
  data() {
    return {
      showHeader: true,
      name: 'Welen',
      lastName: 'Almeida',
      showName: true,
      accessLevel: ''
    }
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
