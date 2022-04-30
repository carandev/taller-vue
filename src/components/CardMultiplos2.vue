<script setup>
import {ref} from 'vue'

const numbers = ref([])
const numberInput = ref(0)
const show = ref(false)
const showInput = ref(true)

const pushNumbers = () => {
  if (numberInput.value === null){
    numbers.value.push(0)
  } else {
    numbers.value.push(numberInput.value)
  }
  numberInput.value = null

  if (numbers.value.length >= 10) {
    showInput.value = false
  }
}
  
const generateNumbers = () => {
  numbers.value = numbers.value.filter(number => number % 2 === 0)
  show.value = true
}

</script>

<template>
  <section class="card">
    <h3>21. Multiplos de 2</h3>
    <label v-if="showInput">
      Numero {{numbers.length + 1}}
      <input type="text" v-model.number="numberInput" class="input" v-on:keyup.enter="pushNumbers">
    </label>
    <button class="button" @click="pushNumbers()" v-if="showInput">Siguiente número</button>
    <button class="button" @click="generateNumbers()" v-if="numbers.length >= 10">Calcular</button>
    <p v-if="show">Multiplos de 2: <br/><span v-for="number in numbers" >{{number + " - "}}</span></p>
  </section>
</template>
