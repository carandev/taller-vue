<script setup>
import {ref} from 'vue'

const numbers = ref([])
const numberInput = ref(0)
const valorNomina = ref(0)
const show = ref(false)
const showInput = ref(true)

const pushNumbers = () => {
  if (numberInput.value === null){
    numbers.value.push(0)
  } else {
    numbers.value.push(numberInput.value)
  }
  numberInput.value = null

  if (numbers.value.length >= 50) {
    showInput.value = false
  }
}
  
const generateNumbers = () => {
  numbers.value = numbers.value.map(number => number * 30_000)

  numbers.value.forEach(number => valorNomina.value += number)
}

</script>

<template>
  <section class="card">
    <h3>27. Calcular Nómina</h3>
    <label v-if="showInput">
      Horas del Empleado {{numbers.length + 1}}
      <input type="text" v-model.number="numberInput" class="input" v-on:keyup.enter="pushNumbers">
    </label>
    <button class="button" @click="pushNumbers()" v-if="showInput">Siguiente empleado</button>
    <button class="button" @click="generateNumbers()" v-if="numbers.length >= 50">Calcular</button>
    <p v-if="valorNomina > 0">El valor de la nómina es: {{valorNomina}}</p>
  </section>
</template>
