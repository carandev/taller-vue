<script setup>
import {ref} from 'vue'

const side = ref(null)
const area = ref(0)

const calculateArea = () => {
  area.value = side.value * side.value
  side.value = null
}
</script>

<template>
  <section class="card">
    <h3>1. Área del cuadrado</h3>
    <label for="side">
      Tamaño del lado (cm)
    </label>
    <input class="input" type="text" id="side" v-model.number="side" @keyup.enter="calculateArea">
    <button class="button" @click="calculateArea">Calcular área</button>
    <p v-if="area > 0">El área es: {{area}} cm</p>
  </section>
</template>

