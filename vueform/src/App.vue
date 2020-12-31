<template>
  <div id="app">
    
    <VueForm msg="Formulario"/>

    <vue-button/>
    <to-dos v-bind="todos"/>
  </div>
</template>

<script>
import ToDos from './components/ToDos.vue'
import VueButton from './components/VueButton.vue'
import VueForm from './components/VueForm.vue'

export default {
  name: 'App',
  components: {
    VueForm,
    VueButton,
    ToDos
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
