<script setup>
import {ref} from 'vue'

const n1 = ref(0)
const n2 = ref(0)
const n3 = ref(0)
const name = ref('')
const notaFinal = ref(0)

const handleClick = () => {

  notaFinal.value = ((n1.value + n2.value + n3.value) / 3).toFixed(2)
}

</script>
<template>
  <section class="card">
    <h3>26. Calcular Nota final</h3>
    <label>
      Nombre
      <input type="text" class="input" v-model="name">
    </label>
    <label>
      Nota 1
      <input type="text" class="input" v-model.number="n1">
    </label>
    <label>
      Nota 2
      <input type="text" class="input" v-model.number="n2">
    </label>
    <label>
      Nota 3
      <input type="text" class="input" v-model.number="n3">
    </label>
    <button class="button" @click="handleClick">Calcular</button>
    <p v-if="notaFinal > 0">Nota Final de {{name}} {{notaFinal}}</p>
  </section>
</template>
