<template>
  <header>
    <img src="../assets/g-dino.png" alt="Dinosaur Logo" />
  </header>
</template>

<script>
export default {
  name: 'dinoHeader',
  data(){
    return {

  }
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  grid-row: 1 / 2;
  display: grid;
  grid-template-columns: 25% 50% 15%;
  grid-template-rows: 50% 50%;
  padding-top: 10px;
}

header img {
  grid-row: 1/3;
  grid-column: 1/2;
  height: 100px;
  width: auto;
}
</style>
