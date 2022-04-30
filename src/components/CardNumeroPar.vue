<script setup>
import {ref} from 'vue'

const number = ref(null)
const par = ref('')

const handleClick = () => {
  if (number.value % 2 === 0) {
    par.value = "par"
  } else {
    par.value = "impar"
  }
}
</script>

<template>
  <section class="card">
    <h3>18. Par o Impar</h3>
    <label for="side">
      Numero
    </label>
    <input class="input" type="text" id="side" v-model.number="number" @keyup.enter="calculateArea">
    <button class="button" @click="handleClick">Calcular</button>
    <p v-if="par !== ''">El número es: {{par}}</p>
  </section>
</template>

