<template>
  <div id="app">
    <galery/>
    <calculadora titulo="sumar" boton="+" opc='1' />
    <calculadora titulo="restar" boton="-" opc='2' />
    <calculadora titulo="multiplicar" boton="x" opc='3'/>
    <calculadora titulo="dividir" boton="/" opc='4'/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import calculadora from './components/calculadora.vue'
import galery from './components/galery.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    calculadora,
    galery
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
  margin-top: 60px;
}
</style>
