<script setup>
import {ref} from 'vue'

const radio = ref(null)
const altura = ref(null)
const area = ref(0)
const volumen = ref(0)

const calculateHipotenusa = () => {
  area.value = ((2 * Math.PI * radio.value * altura.value) + (2 * Math.PI * Math.pow(radio.value, 2))).toFixed(2)
  volumen.value = (Math.PI * Math.pow(radio.value, 2) * altura.value).toFixed(2)
}
</script>

<template>
  <section class="card">
    <h3>17. Area y Volumen del Cilindro</h3>
    <label for="base">
      Radio
    </label>
    <input class="input" type="text" id="base" v-model.number="radio">
    <label for="height">
      Altura
    </label>
    <input class="input" type="text" id="height" v-model.number="altura" @keyup.enter="calculateArea">
    <button class="button" @click="calculateHipotenusa">Calcular área y volumen</button>
    <p v-if="area > 0">El area es: {{area}}</p>
    <p v-if="volumen > 0">El volumen es: {{volumen}}</p>
  </section>
</template>

