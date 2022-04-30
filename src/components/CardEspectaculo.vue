<script setup>
import {ref} from 'vue'

const entradas = ref(0)
const valorEntrada = ref(0)

const handleClick = () => {
  valorEntrada.value = entradas.value * 10_000

  if (entradas.value === 2) {
    valorEntrada.value -= valorEntrada.value * 0.10
  } else if (entradas.value === 3) {
    valorEntrada.value -= valorEntrada.value * 0.15
  } else if (entradas.value === 4){
    valorEntrada.value -= valorEntrada.value * 0.20
  }
}

</script>
<template>
  <section class="card">
    <h3>24. Valor entradas</h3>
    <label>
      Numero de entradas
      <input type="text" class="input" v-model.number="entradas">
    </label>
    <button v-if="entradas <= 4" class="button" @click="handleClick">Calcular</button>
    <p v-if="entradas > 4">Máximo 4 entradas</p>
    <p v-if="valorEntrada > 0">El valor de las entradas es {{valorEntrada}}</p>
  </section>
</template>
