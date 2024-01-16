<template>
  <!-- <TheHeader v-if="showHeader">
  
    <template v-slot:title>
      Titulo
    </template>
    <template v-slot:description>
     <div> Descrição</div>
    </template>
    lorem ipsolum!

  </TheHeader> -->
  <div class="card">Teste</div>
  <BaseCard></BaseCard>
  <!-- <TheForm></TheForm> -->
  <br><br>
  <!-- <TheComputed></TheComputed> -->
  <TheWatch/>
</template>

<script>
// import TheHeader from './components/TheHeader.vue';
// import TheForm from './components/TheForm.vue';
// import TheComputed from './components/TheComputed.vue';
// import TheWatch from './components/TheWatch.vue';
import BaseCard from './components/BaseCard.vue';

export default {
  name: 'App',
  components: {
    // TheHeader,
    // TheForm,
    // TheComputed,
    // TheWatch
    BaseCard
  }, 
  data() {
    return {
      showHeader: true,
      name: 'Welen',
      lastName: 'Almeida',
      showName: true,
      accessLevel: ''
    }
  },
  mounted() {
    console.log(this.$slots);
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
