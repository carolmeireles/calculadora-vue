<script setup>

import { reactive } from 'vue';
import Operacao from "./components/Operacao.vue";

const estado = reactive({
    filtro: 'soma',
    num1: 0,
    num2: 0
});

function realizaOperacao() {
    const { filtro, num1, num2 } = estado;
    switch (filtro) {
      case 'soma':
        return num1 + num2;
      case 'subtracao':
        return num1 - num2;
      case 'multiplicacao':
        return num1 * num2;
      case 'divisao':
        return num1 / num2;
    }
}

</script>

<template>

<div class="container">
  <header class="pt-5 pb-5 mt-4">
    <h1>Calculadora Aritmética</h1>
</header>

  <Operacao
    :filtrar-operacao="(event) => (estado.filtro = event.target.value)"
    :numero1="(event) => (estado.num1 = Number(event.target.value))"
    :numero2="(event) => (estado.num2 = Number(event.target.value))" />
  
  <p>
    O resultado da operação é... {{ realizaOperacao() }}
  </p>
 
</div>

</template>

<style scoped>

</style>
