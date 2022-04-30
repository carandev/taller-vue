<script setup>
import {ref} from 'vue'

const number1 = ref(null)
const number2 = ref(null)
const number3 = ref(null)
const higherNumber = ref(0)
const lowerNumber = ref(0)
const equals = ref(false)

const calculateHigherNumber = () => {
  if (number1.value === number2.value || number2.value === number3.value || number3.value === number1.value) {
    equals.value = true
  } else {
    higherNumber.value = Math.max(number1.value, number2.value, number3.value)
    lowerNumber.value = Math.min(number1.value, number2.value, number3.value)
    equals.value = false
  }
}

</script>

<template>
  <section class="card">
    <h3>10. Mayor y menor de tres números</h3>
    <label>
      Numero 1:
      <input class="input" type="text" v-model.number="number1">
    </label>
    <label>
      Numero 2:
      <input class="input" type="text" v-model.number="number2">
    </label>
    <label>
      Numero 3:
      <input class="input" type="text" v-model.number="number3">
    </label>
    <button class="button" @click="calculateHigherNumber">Calcular</button>
    <div>
      <p v-if="!equals">Mayor: {{higherNumber}} <br/> Menor: {{lowerNumber}}</p>
      <p v-if="equals">Deben ser valores diferentes</p>
    </div>
  </section>
</template>
