<script setup>
import {ref} from 'vue'

const kilometros = ref(0)
const metros = ref(0)

const handleClick = () => {
  metros.value = kilometros.value * (5/18)
}

</script>
<template>
  <section class="card">
    <h3>25. Pasar de k/h a m/s</h3>
    <label>
      k/h
      <input type="text" class="input" v-model.number="kilometros">
    </label>
    <button class="button" @click="handleClick">Calcular</button>
    <p v-if="metros > 0">Son {{metros}} m/s</p>
  </section>
</template>
