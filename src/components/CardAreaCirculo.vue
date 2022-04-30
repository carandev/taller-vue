<script setup>
import {ref} from 'vue'

const radio = ref(null)
const area = ref(0)

const calculateArea = () => {
  area.value = (Math.PI * Math.pow(radio.value, 2)).toFixed(2)
  base.value = null
  height.value = null
}
</script>

<template>
  <section class="card">
    <h3>2. Área del Círculo</h3>
    <label for="base">
      Radio (cm)
    </label>
    <input class="input" type="text" id="base" v-model.number="radio">
    <button class="button" @click="calculateArea">Calcular área</button>
    <p v-if="area > 0">El área es: {{area}} cm</p>
  </section>
</template>

