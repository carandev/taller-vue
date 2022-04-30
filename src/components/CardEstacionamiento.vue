<script setup>
import {ref} from 'vue'

const hours = ref(0)
const tarifa = ref(0)

const handleClick = () => {
  if (hours.value > 1) {
    tarifa.value = (hours.value - 1) * 2_000
    tarifa.value += 3_000
  } else {
    tarifa.value = 3_000
  }
}

</script>
<template>
  <section class="card">
    <h3>23. Tarifa estacionamiento</h3>
    <input type="text" class="input" v-model.number="hours">
    <button class="button" @click="handleClick">Calcular</button>
    <p v-if="tarifa > 0">La tarifa es {{tarifa}}</p>
  </section>
</template>
