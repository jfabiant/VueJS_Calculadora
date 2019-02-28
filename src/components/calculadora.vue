<template>
  <div class="red">
    <center>
      <h1 color="red--text">{{titulo}}</h1>
    </center>
    <input type="text" v-model="numero1">
    <input type="text" v-model="numero2">
    <button @click="operacion()">{{boton}}</button>
    <center>
      <h3>Resultado: {{resultado}}</h3>
    </center>
  </div>
</template>
<script>
export default {
  props: ["titulo", "boton", "opc"],
  name: "calculadora",
  data() {
    return {
      numero1: null,
      numero2: null,
      resultado: null
    };
  },
  methods: {
    operacion() {
      // console.log(this.numero1);
      // console.log(this.numero2);
      if (this.opc == 1) {
        //Sumar
        const res = parseFloat(this.numero1) + parseFloat(this.numero2);
        this.resultado = res;
      } else if (this.opc == 2) {
        //Restar
        let res = parseFloat(this.numero1) - parseFloat(this.numero2);
        this.resultado = res;
      } else if (this.opc == 3) {
        //Multiplicar
        let res = parseFloat(this.numero1) * parseFloat(this.numero2);
        this.resultado = res;
      } else {
        //Dividir
        let res = parseFloat(this.numero1) / parseFloat(this.numero2);
        this.resultado = res;
      }
    }
  }
};
</script>
