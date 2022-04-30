<script setup>
import {ref} from 'vue'

const a = ref(0)
const b = ref(0)
const c = ref(0)
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
  numbers.value.forEach(number => {
    if (number >= 50 && number <= 75){
      a.value++
    } else if (number > 80){
      b.value++
    } else if (number < 30) {
      c.value++
    }
  })
}

</script>

<template>
  <section class="card">
    <h3>19. Rangos</h3>
    <label>
      Numero {{numbers.length + 1}}
      <input v-if="numbers.length < 9" type="text" v-model.number="numberInput" class="input" v-on:keyup.enter="pushNumbers">
    </label>
    <button class="button" @click="pushNumbers()" v-if="numbers.length < 9">Siguiente número</button>
    <button class="button" @click="generateNumbers()" v-if="numbers.length >= 9">Calcular</button>
    <p>Entre 50 y 75: {{a}}<br/>Mayor a 80: {{b}}<br/>Menor a 30: {{c}}</p>
  </section>
</template>
