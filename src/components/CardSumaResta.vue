<script setup>
import {ref} from 'vue'

const number1 = ref(null)
const number2 = ref(null)
const resultAdd = ref(null)
const resultSubstract = ref(null)

const add = () => {
  resultAdd.value = number1.value + number2.value
}

const substract = () => {
  resultSubstract.value = number1.value - number2.value
}
</script>

<template>
  <section class="card">
    <h3>4. Suma y Resta</h3>
    <label>
      Numero 1:
      <input class="input" type="text" v-model.number="number1">
    </label>
    <label>
      Numero 2:
      <input class="input" type="text" v-model.number="number2">
    </label>
    <button class="button" @click="add">Sumar</button>
    <button class="button" @click="substract">Restar</button>
    <div>
      <p v-if="resultAdd > 0">Resultado de la suma: {{resultAdd}}</p>
      <p v-if="resultSubstract !== null">Resultado de la resta: {{resultSubstract}}</p>
    </div>
  </section>
</template>
