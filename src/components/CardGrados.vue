<script setup>
import {ref} from 'vue'

const grade = ref(null)
const farenheit = ref(0)

const calculateGrade = () => {
  farenheit.value = (grade.value * 1.8) + 32
  grade.value = null
}
</script>

<template>
  <section class="card">
    <h3>3. Grados Celsius a Farenheit</h3>
    <label for="grade">
      Grados Celsius
    </label>
    <input class="input" type="text" id="grade" v-model.number="grade" @keyup.enter="calculateGrade">
    <button class="button" @click="calculateGrade">Calcular grados en Farenheit</button>
    <p v-if="farenheit > 0">Son {{farenheit}} grados Farenheit</p>
  </section>
</template>
