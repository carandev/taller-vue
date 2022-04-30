<script setup>
import {ref} from 'vue'

const numbers = ref([])

const generateNumbers = () => {
  for (let i = 1; i <= 7; i++) {
    numbers.value.push(i)
  }
}
  
</script>

<template>
  <section class="card">
    <h3>8. Serie de 7</h3>
    <button class="button" @click="generateNumbers">Generar números</button>
    <p> <span class="number" v-for="number in numbers" :key="number"> {{number}} </span> </p>
  </section>
</template>

<style scoped>
.number {
  padding: 0 .5rem;
}
</style>
