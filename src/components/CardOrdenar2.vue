<script setup>
import {ref} from 'vue'

const number1 = ref(null)
const number2 = ref(null)
const higherNumber = ref(0)
const lowerNumber = ref(0)
const show = ref(false)

const calculateHigherNumber = () => {
  if (number1.value > number2.value){
    higherNumber.value = number1
    lowerNumber.value = number2
  } else {
    higherNumber.value = number2
    lowerNumber.value = number1
  }

  show.value = true
}

</script>

<template>
  <section class="card">
    <h3>20. Ordenar dos numero</h3>
    <label>
      Numero 1:
      <input class="input" type="text" v-model.number="number1">
    </label>
    <label>
      Numero 2:
      <input class="input" type="text" v-model.number="number2">
    </label>
    <button class="button" @click="calculateHigherNumber">Calcular mayor número</button>
    <div v-if="show">
      <p>Menor {{lowerNumber}}</p>
      <p>Mayor {{higherNumber}}</p>
      <p v-if="number1 === number2">Los números son iguales</p>
    </div>
  </section>
</template>
