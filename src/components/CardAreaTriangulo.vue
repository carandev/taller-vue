<script setup>
import {ref} from 'vue'

const base = ref(null)
const height = ref(null)
const area = ref(0)

const calculateArea = () => {
  area.value = (base.value * height.value)/2
  base.value = null
  height.value = null
}
</script>

<template>
  <section class="card">
    <h3>6. Área del Triángulo</h3>
    <label for="base">
      Base (cm)
    </label>
    <input class="input" type="text" id="base" v-model.number="base">
    <label for="height">
      Altura (cm)
    </label>
    <input class="input" type="text" id="height" v-model.number="height" @keyup.enter="calculateArea">
    <button class="button" @click="calculateArea">Calcular área</button>
    <p v-if="area > 0">El área es: {{area}} cm</p>
  </section>
</template>

