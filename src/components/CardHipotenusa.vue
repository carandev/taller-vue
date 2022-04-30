<script setup>
import {ref} from 'vue'

const cateto1 = ref(null)
const cateto2 = ref(null)
const hipotenusa = ref(0)

const calculateHipotenusa = () => {
  hipotenusa.value = Math.pow(cateto1.value, 2) + Math.pow(cateto2.value, 2)
}

</script>

<template>
  <section class="card">
    <h3>16. Hipotenusa del Triángulo</h3>
    <label for="base">
      Cateto 1
    </label>
    <input class="input" type="text" id="base" v-model.number="cateto1">
    <label for="height">
      Cateto 2
    </label>
    <input class="input" type="text" id="height" v-model.number="cateto2" @keyup.enter="calculateArea">
    <button class="button" @click="calculateHipotenusa">Calcular Hipotenusa</button>
    <p v-if="hipotenusa > 0">La hipotenusa es: {{hipotenusa}}</p>
  </section>
</template>

