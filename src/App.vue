<template>
  <div id="app">
      <dinoHeader/>
    <main>
      <jobDetails/>
      <inputForm/>
    </main>
    <dinoFooter/>
  </div>
</template>

<script>
import dinoHeader from './components/dinoHeader.vue'
import dinoFooter from './components/dinoFooter.vue'
import jobDetails from './components/jobDetails.vue'
import inputForm from './components/inputForm.vue'
export default {
  name: 'App',
  components: {
    dinoHeader,
    dinoFooter,
    jobDetails,
    inputForm,
  }
}
</script>

<style>
html {
  margin: 0;
  padding: 0;
}

body {
  margin: 0 30px 0 30px;
  padding: 0;
  font-family: sans-serif;
  color: #1B997A;
  display: grid;
  grid-template-rows: 15% 75% 10%;
}

main {
  grid-row: 2/3;
  width: 70%;
  margin: 0 auto;
  padding: 10px;
}
</style>
