<script setup>
import {ref} from 'vue'

const sumatoria = ref(0)
const cantidadImpares = ref(0)
const numbers = ref([])
const numberInput = ref(0)
const show = ref(false)

const pushNumbers = () => {
  if (numberInput.value === null){
    numbers.value.push(0)
  } else {
    numbers.value.push(numberInput.value)
  }
  numberInput.value = null
}
  
const generateNumbers = () => {
  sumatoria.value = 0
  numbers.value.forEach(number => {
    if (number % 2 !== 0) {
      sumatoria.value += number
      cantidadImpares.value++
    }
  })

  show.value = true
}

</script>

<template>
  <section class="card">
    <h3>15. Sumatoria Impares del 1 - 300</h3>
    <label>
      Numero {{numbers.length + 1}}
      <input v-if="numbers.length < 299" type="text" v-model.number="numberInput" class="input" v-on:keyup.enter="pushNumbers">
    </label>
    <button class="button" @click="pushNumbers()" v-if="numbers.length < 299">Siguiente número</button>
    <button class="button" @click="generateNumbers()" v-if="numbers.length >= 299">Calcular</button>
    <p v-if="show">Hay {{cantidadImpares}} números impares</p>
    <p v-if="show">Sumatoria: {{sumatoria}}</p>
  </section>
</template>
