<script setup>
import {ref} from 'vue'

const sumatoria = ref(0)

const generateNumbers = () => {
  const numbers = []
  sumatoria.value = 0
  for (let i = 1; i <= 10; i++) {
    numbers.push(i)
  }

  numbers.forEach(number => sumatoria.value+=number)
}
  
</script>

<template>
  <section class="card">
    <h3>12. Sumatoria de 10 números enteros</h3>
    <button class="button" @click="generateNumbers">Generar números</button>
    <p>Sumatoria {{sumatoria}}</p>
  </section>
</template>

