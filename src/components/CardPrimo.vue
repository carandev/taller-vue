<script setup>
import {ref} from 'vue'

const n = ref(0)
const primo = ref(null)

function handleClick () {
    let cd = 0;
    for (let i = 1; i <= n.value; i++) {
      if (n.value % i == 0) {
        ++cd;
      }
    }
    primo.value = cd <= 2
}

</script>

<template>
  <section class="card">
    <h3>30. Es primo?</h3>
    <label>
      <input type="text" class="input" v-model.number="n">
    </label>
    <button class="button" @click="handleClick">Calcular</button>
    <p v-if="primo">Es primo</p>
    <p v-if="!primo">No es primo</p>
  </section>
</template>
