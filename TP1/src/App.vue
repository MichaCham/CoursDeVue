<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from './components/km.vue'
import Km from './components/km.vue';
import ListeLegume from './components/listeLegume.vue';
import ListeLegume1 from './components/listeLegume.vue';
import Carrousel from './components/Carrousel.vue';
</script>

<template>
  <Km/>
  <ListeLegume/>
  <Carrousel/>
</template>

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
