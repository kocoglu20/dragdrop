<template>
  <div id="app">
    {{fatura.adi}}
    {{fatura.soyadi}}
  </div>
</template>

<script>

export default {
  name: 'app',
  data(){
    return {
      fatura:{
        adi:'Ahmet',
        soyadi:'Koçoğlu'
      }
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;

}
</style>
