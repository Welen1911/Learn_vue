<template>
  <!-- <TheHeader v-if="showHeader"/> -->
  <TheForm></TheForm>
</template>

<script>
// import TheHeader from './components/TheHeader.vue';
import TheForm from './components/TheForm.vue';

export default {
  name: 'App',
  components: {
    // TheHeader
    TheForm
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
