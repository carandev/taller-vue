<script setup>
import {ref} from 'vue'

const number1 = ref(null)
const number2 = ref(null)
const number3 = ref(null)
const higherNumber = ref(0)
const equals = ref(false)

const calculateHigherNumber = () => {
  if (number1.value === number2.value || number2.value === number3.value || number3.value === number1.value) {
    equals.value = true
  } else {
    if (number1.value > number2.value && number1.value > number3.value) { higherNumber.value = number1.value
    } else if (number2.value > number1.value && number2.value > number3.value) {
      higherNumber.value = number2.value
    } else if (number3.value > number1.value && number3.value > number2.value) {
      higherNumber.value = number3.value
    }

    equals.value = false
  }
}

</script>

<template>
  <section class="card">
    <h3>7. Mayor de tres números</h3>
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
    <button class="button" @click="calculateHigherNumber">Calcular mayor número</button>
    <div>
      <p v-if="higherNumber !== 0">Mayor número {{higherNumber}}</p>
      <p v-if="equals">Los valores deben ser diferentes</p>
    </div>
  </section>
</template>
