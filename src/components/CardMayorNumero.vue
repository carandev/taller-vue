<script setup>
import {ref} from 'vue'

const number1 = ref(null)
const number2 = ref(null)
const higherNumber = ref(0)

const calculateHigherNumber = () => {
  if (number1.value > number2.value) {
    higherNumber.value = number1.value
  } else {
    higherNumber.value = number2.value
  }
}

</script>

<template>
  <section class="card">
    <h3>5. Mayor de dos números</h3>
    <label>
      Numero 1:
      <input class="input" type="text" v-model.number="number1">
    </label>
    <label>
      Numero 2:
      <input class="input" type="text" v-model.number="number2">
    </label>
    <button class="button" @click="calculateHigherNumber">Calcular mayor número</button>
    <div>
      <p v-if="number1 !== number2">El mayor número es: {{higherNumber}}</p>
      <p v-if="number1 === number2">Los números son iguales</p>
    </div>
  </section>
</template>
