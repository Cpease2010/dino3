<template>
  <div id="app">
    <dinoHeader/>
    <dinoFooter/>
  </div>
</template>

<script>
import dinoHeader from './components/dinoHeader.vue'
import dinoFooter from './components/dinoFooter.vue'
export default {
  name: 'App',
  components: {
    dinoHeader,
    dinoFooter
  }
}
</script>

<style>

</style>
