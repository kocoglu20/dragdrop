<template>
  <div id="app">
    <h4>
      {{fatura.adi}}
      {{fatura.clientX.toFixed(0)}}
      {{fatura.clientY.toFixed(0)}}
    </h4>
    <div id="a4" @mousemove="yakala" @mouseout="cikti" @click="tikladi" @dblclick="tiklaiptal" ref="yakala">

    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return {
      fatura:{
        dur: false,
        adi: 'Fatura Dizaynı',
        clientX: 0,
        clientY: 0
      }
    }
  },
  methods:{
    yakala(event){
      if (this.fatura.dur === false) {
        this.fatura.clientX = event.clientX - this.$refs.yakala.getBoundingClientRect().left;
        this.fatura.clientY = event.clientY - this.$refs.yakala.getBoundingClientRect().top;
      }
    },
    cikti(){
      this.fatura.clientX=0;
      this.fatura.clientY=0;
    },
    tikladi(){
      this.fatura.dur = true;
    },
    tiklaiptal(){
      this.fatura.dur = false;
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
#app h4{
  margin: 0;
  padding: 0 0 5px 0;
}
#a4{
  width: 200mm;
  height: 287mm;
  border: 1px solid #000000;
  margin: 0 auto;
}
</style>
