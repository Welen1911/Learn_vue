<template>
  <!-- <TheHeader v-if="showHeader"/> -->
  <!-- <TheForm></TheForm> -->
  <br><br>
  <TheComputed></TheComputed>
</template>

<script>
// import TheHeader from './components/TheHeader.vue';
// import TheForm from './components/TheForm.vue';
import TheComputed from './components/TheComputed.vue';

export default {
  name: 'App',
  components: {
    // TheHeader
    // TheForm,
    TheComputed,
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
