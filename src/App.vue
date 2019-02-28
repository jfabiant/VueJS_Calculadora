<template>
  <div id="app">
    <galery/>
    <label>Numerador Izquierdo</label>
    <input type="text" v-model="numero1">
    <calculadora titulo="sumar" boton="+" opc='1' :numero1="numero1"/>
    <calculadora titulo="restar" boton="-" opc='2' :numero1="numero1"/>
    <calculadora titulo="multiplicar" boton="x" opc='3' :numero1="numero1"/>
    <calculadora titulo="dividir" boton="/" opc='4' :numero1="numero1"/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import calculadora from './components/calculadora.vue'
import galery from './components/galery.vue'

export default {
  name: 'app',
  components: {
    // HelloWorld,
    calculadora,
    galery
  },  data() {
    return {
      numero1: null,
    };
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
