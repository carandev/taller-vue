<script setup>
import {ref} from 'vue'

const number1 = ref(null)
const number2 = ref(null)
const higherNumber = ref(0)
const lowerNumber = ref(0)

const calculateHigherNumber = () => {
  if (number1.value > number2.value){
    higherNumber.value = number1.value
    lowerNumber.value = number2.value
  } else {
    higherNumber.value = number2.value
    lowerNumber.value = number1.value
  }
}

</script>

<template>
  <section class="card">
    <h3>9. Mayor y menor de dos números</h3>
    <label>
      Numero 1:
      <input class="input" type="text" v-model.number="number1">
    </label>
    <label>
      Numero 2:
      <input class="input" type="text" v-model.number="number2">
    </label>
    <button class="button" @click="calculateHigherNumber">Calcular</button>
    <div>
      <p>Mayor: {{higherNumber}} <br/> Menor: {{lowerNumber}}</p>
    </div>
  </section>
</template>
