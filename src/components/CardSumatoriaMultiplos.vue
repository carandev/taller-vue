<script setup>
import {ref} from 'vue'

const sumatoria = ref(0)
const numbers = ref([])

const generateNumbers = () => {
  numbers.value = []
  sumatoria.value = 0
  for (let i = 1; i <= 100; i++) {
    if (i % 5 == 0) {
      numbers.value.push(i)
    }
  }

  numbers.value.forEach(number => sumatoria.value+=number)
}

</script>

<template>
  <section class="card">
    <h3>13. Sumatoria múltiplos de 5 del 1 - 100</h3>
    <button class="button" @click="generateNumbers()">Generar números</button>
    <p>Numeros: <span v-for="number in numbers" :key="number">{{number + "-"}}</span></p>
    <p>Sumatoria: {{sumatoria}}</p>
  </section>
</template>

